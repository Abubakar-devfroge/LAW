<script>
	import '@fontsource-variable/ibm-plex-sans';
	let { children } = $props();
	import '../app.css';
</script>


<svelte:head>
	<title>OMA ADVOCATES - Legal Firm</title>
	<meta name="description" content="Get legal counsel from top laywers." />
</svelte:head>

<main class="pt-4">
	{@render children()}
</main>
