<script>
  import favicon from '$lib/assets/favicon.svg';
  import { afterNavigate } from '$app/navigation'; 

  let mobileOpen = false;

  let navs = [
    { name: 'About us', href: '/about' },
    { name: 'What we do', href: '/' },
    { name: 'Why us', href: '/' },
    { name: 'Careers', href: '/' }
  ];

  let Logo = '/icon.png';
  let menu = '/ham.svg';
  let close = '/menu.svg';


  afterNavigate(() => {
    mobileOpen = false;
  });
</script>


<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

<header class="bg-white backdrop-blur top-0 z-50 font-sans ">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16">

 
      <div class="flex items-center">
        <img class="h-8 w-auto" src={Logo} alt="Logo" />
        <span class="ml-3 text-xl font-semibold text-gray-900 leading-tight">
          OMA <br>& Associates
        </span>
      </div>

      
      <nav class="hidden md:flex space-x-8">
        {#each navs as nav}
          <a 
            href={nav.href}
            class="relative text-lg font-semibold tracking-wide uppercase text-gray-900 pb-1
                   before:absolute before:bottom-0 before:left-0 before:h-[3px] before:w-full 
                   before:bg-blue-800 before:origin-left before:scale-x-0 
                   before:transition-transform before:duration-300 hover:before:scale-x-100"
          >
            {nav.name}
          </a>
        {/each}
      </nav>

   
      <button 
        on:click={() => mobileOpen = !mobileOpen}
        aria-expanded={mobileOpen}
        class="md:hidden flex items-center justify-center p-2 rounded-md text-gray-700 hover:bg-gray-100 transition"
      >
        <span class="sr-only">Toggle navigation</span>
        {#if !mobileOpen}
        <img 
          src={menu}
          alt="Menu" 
          class="h-10 w-10 object-contain"
        />
      {:else}

           <img 
          src={close}
          alt="Menu" 
          class="h-10 w-10 object-contain"
        />
        {/if}
      </button>

    </div>
  </div>

  <!-- Mobile Menu -->
  <div
    class={`md:hidden transition-all duration-300 ease-in-out overflow-hidden bg-white 
      ${mobileOpen ? "max-h-96 opacity-100" : "max-h-0 opacity-0"}`}
  >
    <div class="px-4 pt-4 pb-6 space-y-4 flex flex-col items-start">
      {#each navs as nav}
        <a 
          href={nav.href} 
       
          class="relative text-lg font-semibold tracking-wide uppercase text-gray-900 pb-1
                   before:absolute before:bottom-0 before:left-0 before:h-[3px] before:w-full 
                   before:bg-blue-800 before:origin-left before:scale-x-0 
                   before:transition-transform before:duration-300 hover:before:scale-x-100"
          >
          {nav.name}
        </a>
      {/each}
    </div>
  </div>
</header>
