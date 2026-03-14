<script>
 
import '@fontsource-variable/ibm-plex-sans';
	import Footer from '$lib/components/Footer.svelte';
  let { children } = $props();
   import "../app.css";
</script>




<main class="pt-4">
	
  {@render children()}
</main>


<Footer />