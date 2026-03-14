<script lang="ts">
	import { resolve } from '$app/paths';
	import { enhance } from '$app/forms';

	let bg = '/contract.webp';
	let img = '/logo.webp';

	let form = {
		fullName: '',
		email: '',
		phone: '',
		availability: ''
	};

	let status: { success?: boolean; error?: string } = {};
</script>

<div class="min-h-screen grid grid-cols-1 lg:grid-cols-2">
	<div class="flex bg-white items-center justify-center p-14">
		<div class="w-full max-w-md">
			<a href={resolve('/')} class="inline-block">
				<img
					src={img}
					alt="Law firm logo"
					class="h-32 sm:h-40 w-auto"
					width="299"
					height="224"
					fetchpriority="high"
					on:contextmenu|preventDefault
				/>
			</a>

			<form
				class="mt-4 space-y-5"
				method="POST"
				use:enhance={() => {
					return async ({ result, update }) => {
						if (result.type === 'success') {
							if (result.data?.success) {
								status = { success: true };
								// Reset form
								form = { fullName: '', email: '', phone: '', availability: '' };
							} else {
								status = {
									success: false,
									error: String(result.data?.error || 'Submission failed')
								};
							}
						} else if (result.type === 'error') {
							status = { success: false, error: 'Submission failed' };
							console.error(result.error);
						}
						await update();
					};
				}}
			>
				<div class="space-y-1.5">
					<label for="fullName" class="text-sm font-medium text-gray-700"> Name </label>
					<input
						id="fullName"
						name="fullName"
						placeholder="Your name"
						type="text"
						bind:value={form.fullName}
						required
						class="w-full rounded-md border border-gray-300 bg-white px-4 py-2 text-gray-900
						placeholder:text-gray-400
						focus:border-blue-600 focus:ring-4 focus:ring-blue-600/10
						transition"
					/>
				</div>

				<div class="space-y-1.5">
					<label for="email" class="text-sm font-medium text-gray-700"> Email </label>
					<input
						id="email"
						name="email"
						type="email"
						placeholder="Your email"
						bind:value={form.email}
						required
						class="w-full rounded-md border border-gray-300 bg-white px-4 py-2 text-gray-900
						placeholder:text-gray-400
						focus:border-blue-600 focus:ring-4 focus:ring-blue-600/10
						transition"
					/>
				</div>

				<div class="space-y-1.5">
					<label for="availability" class="text-sm font-medium text-gray-700">
						Your messsage
					</label>
					<input
						id="availability"
						name="availability"
						type="text"
						bind:value={form.availability}
						class="w-full rounded-md border border-gray-300 bg-white px-4 py-2 text-gray-900
						focus:border-blue-600 focus:ring-4 focus:ring-blue-600/10
						transition"
					/>
				</div>

				<button
					type="submit"
					class="mt-4 w-full rounded-md bg-[#245524]
					py-2 text-sm font-semibold text-white
					hover:bg-[#245524]
					active:scale-[0.98]
					transition-all"
				>
					Send Message
				</button>
			</form>

			<!-- Terms agreement -->
			<div class="mt-4 mb-10 flex items-start gap-3 text-sm text-gray-600">
				<p class="leading-relaxed">
					By clicking Send Message, I agree to the
					<a
						href="/Terms"
						target="_blank"
						class="font-medium text-gray-900 underline underline-offset-4 hover:text-[#245524]"
					>
						Terms of Service
					</a>
					and
					<a
						href="/Privacy"
						target="_blank"
						class="font-medium text-gray-900 underline underline-offset-4 hover:text-[#245524]"
					>
						Privacy Policy
					</a>.
				</p>
			</div>
		</div>
	</div>

	<div
		class="lg:flex text-white items-center justify-center bg-cover bg-center"
		style="background-image: url({bg}); user-select: none;"
	>
		<!-- Success/Error message -->
		{#if status.success || status.error}
			<div
				class="fixed top-5 left-1/2 transform -translate-x-1/2 px-6 py-3 rounded-md shadow-lg flex items-center space-x-3
           text-white animate-slideIn fade-out
           {status.success ? 'bg-green-600' : 'bg-red-600'}"
			>
				{#if status.success}
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
					</svg>
					<span>
						Thank you for applying! We’ve received your application successfully. Keep an eye on
						your inbox — we’ll be in touch soon with the next steps.
					</span>
				{:else}
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
					<span>{status.error}</span>
				{/if}
			</div>
		{/if}
	</div>
</div>

<style>
	@keyframes slideIn {
		0% {
			opacity: 0;
			transform: translateX(-50%) translateY(-20px);
		}
		100% {
			opacity: 1;
			transform: translateX(-50%) translateY(0);
		}
	}

	.animate-slideIn {
		animation: slideIn 0.3s ease-out forwards;
	}

	@keyframes fadeOut {
		0% {
			opacity: 1;
		}
		100% {
			opacity: 0;
		}
	}

	.fade-out {
		animation: fadeOut 0.5s ease-in 3s forwards; /* fades out after 3 seconds */
	}
</style>
