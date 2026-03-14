<script>
	import { resolve } from '$app/paths';
	let img = '/logo.webp';
</script>

<div class="min-h-screen flex flex-col text-gray-800">
	<header class="flex items-center justify-between px-8 py-6 bg-white">
		<div class="flex items-center gap-4">
			<a href={resolve('/')} class="inline-block">
				<img
					src={img}
					alt="Lawfirm  logo"
					class="h-22 sm:h-22 w-auto"
					fetchpriority="high"
					on:contextmenu|preventDefault
				/>
			</a>

			<span class="h-22 w-px bg-gray-300"></span>

			<h1 class="text-xl sm:text-2xl font-semibold tracking-tight">
				<slot name="title">Page Title</slot>
			</h1>
		</div>
	</header>

	<main class="flex-1 px-8 py-12 max-w-4xl bg-white mx-auto w-full">
		<slot />
		<!-- Page-specific content goes here -->
	</main>

	<footer class="flex justify-end px-8 py-6 bg-white">
		<div class="flex items-center gap-4 text-sm text-gray-500">
			<span class="h-22 w-px bg-gray-300"></span>
			<span>&copy; {new Date().getFullYear()} Lock.in</span>
			<span>All rights reserved</span>
		</div>
	</footer>
</div>
