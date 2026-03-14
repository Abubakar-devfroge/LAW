<script>
	let img = '/logo.webp';
	import { resolve } from '$app/paths';
	const products = [
		{ label: 'Lockin premium', href: '/premium' },
		{ label: 'Lock.in Swag', href: '/shop' },
		{ label: 'Community', href: '/community' },
		{ label: 'Pricing', href: '/pricing' }
	];

	const company = [
		{ label: 'About us', href: '/' },
		{ label: 'Services', href: '/path' },
		{ label: 'Contact us', href: '/blog' }
	];

	const legal = [
		{ label: 'Terms of use', href: '/Terms' },
		{ label: 'Privacy policy', href: '/Policy' }
	];
</script>

<footer class="bg-white text-gray-700">
	<div class="mx-auto max-w-7xl px-6 py-12 grid grid-cols-1 gap-10 sm:grid-cols-2 md:grid-cols-5">
		<!-- Brand -->
		<aside class="md:col-span-2 space-y-4">
			<span class="text-4xl tracking-tight text-gray-900 font-extrabold mb-4">
				<a href={resolve('/')} class="flex items-center gap-1">
					<img
						src={img}
						alt="OMA &ADVOCATES"
						class="h-24 w-auto"
						width="299"
						height="224"
						fetchpriority="high"
						on:contextmenu|preventDefault
					/>
				</a>
			</span>

			<p class="text-sm leading-relaxed">
				<span class="font-semibold text-gray-900"> OMA &ADVOCATES </span>
				<br />
				Your compass in law.
			</p>
		</aside>

		<!-- Products -->
		<nav class="space-y-3">
			<h6 class="text-sm font-semibold uppercase tracking-wide text-gray-900">Pratise Areas</h6>
			<ul class="space-y-2 text-sm">
				{#each products as item}
					<li>
						<a
							href={resolve(item.href)}
							class="relative inline-block
					after:absolute after:left-0 after:-bottom-1
					after:h-0.5 after:w-full
					after:origin-left after:scale-x-0
					after:bg-[#245524]
					after:transition-transform after:duration-300 after:ease-out
					hover:after:scale-x-100"
						>
							{item.label}
						</a>
					</li>
				{/each}
			</ul>
		</nav>

		<!-- Company -->
		<nav class="space-y-3">
			<h6 class="text-sm font-semibold uppercase tracking-wide text-gray-900">Company</h6>
			<ul class="space-y-2 text-sm">
				{#each company as item}
					<li>
						<a
							href={resolve(item.href)}
							class="relative inline-block
					after:absolute after:left-0 after:-bottom-1
					after:h-0.5 after:w-full
					after:origin-left after:scale-x-0
					after:bg-[#245524]
					after:transition-transform after:duration-300 after:ease-out
					hover:after:scale-x-100"
						>
							{item.label}
						</a>
					</li>
				{/each}
			</ul>
		</nav>

		<!-- Legal -->
		<nav class="space-y-3">
			<h6 class="text-sm font-semibold uppercase tracking-wide text-gray-900">Legal</h6>
			<ul class="space-y-2 text-sm">
				{#each legal as item}
					<li>
						<a
							href={resolve(item.href)}
							class="relative inline-block
					after:absolute after:left-0 after:-bottom-1
					after:h-0.5 after:w-full
					after:origin-left after:scale-x-0
					after:bg-[#245524]
					after:transition-transform after:duration-300 after:ease-out
					hover:after:scale-x-100"
						>
							{item.label}
						</a>
					</li>
				{/each}
			</ul>
		</nav>
	</div>
</footer>
