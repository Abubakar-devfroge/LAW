<script>
	import '@fontsource-variable/ibm-plex-sans';
	let { children } = $props();
	import '../app.css';
</script>

<main class="pt-4">
	{@render children()}
</main>
