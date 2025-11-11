<script>
	import Footer from '$lib/components/Footer.svelte';
  import Header from '$lib/components/Header.svelte'
  let { children } = $props();
   import "../app.css";
</script>



<Header />

<main class="pt-4">
	
  {@render children()}
</main>


<Footer />