<script>
	import { resolve } from '$app/paths';
	let img = '/law.webp';
	let paragraph =
		'Navigate complex legal requirements with clarity, confidence, and informed decision-making.';
</script>

<section class="relative overflow-hidden bg-white">
	<div class="relative mx-auto max-w-7xl px-6 py-4">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
			<div class="max-w-xl">
				<a href={resolve('/')} class="inline-block">
					<img
						src="/law"
						alt="Law logo"
						class="h-32 sm:h-40 w-auto"
						width="299"
						height="224"
						fetchpriority="high"
						on:contextmenu|preventDefault
					/>
				</a>

				<h1 class="mt-8 text-5xl font-extrabold tracking-tight sm:text-6xl text-black">
					Redefining the Art
					<span class="block"> of Law</span>
				</h1>

				<p class="mt-6 lg:text-base sm:text-sm leading-relaxed text-gray-600">
					{paragraph}
				</p>

				<div class="mt-10 flex flex-wrap gap-4">
					<a
						href={resolve('/contact')}
						class="inline-flex items-center justify-center rounded-md bg-[#245524] px-8 py-2 text-base font-medium text-white transition hover:bg-[#245524] focus:outline-none focus:ring-2 focus:ring-[#47c263] focus:ring-offset-2"
					>
						Contact Us
					</a>

					<a
						href={resolve('/about')}
						class="inline-flex items-center justify-center rounded-md bg-gray-100 px-8 py-2 text-base font-medium text-black transition hover:bg-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:ring-offset-2"
					>
						Learn more
					</a>
				</div>
			</div>

			<!-- RIGHT: Hero Image -->
			<div class="relative">
				<div
					class="relative rounded-3xl overflow-hidden w-full h-0"
					style="padding-bottom: 56.25%;"
				>
					<img
						src={img}
						alt="Abstract design"
						class="absolute top-0 left-0 w-full h-full object-cover"
						fetchpriority="high"
						on:contextmenu|preventDefault
					/>
				</div>
			</div>
		</div>
	</div>
</section>
