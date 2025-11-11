<script>
  import favicon from '$lib/assets/favicon.svg';
  let mobileOpen = false;
  let navs = [
    { name: 'About us', href: '/about' },
    { name: 'What we do', href: '/' },
    { name: 'Why us', href: '/' },
    { name: 'Careers', href: '/' }
  ];

  let Logo = '/icon.png';
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

<header class="bg-white backdrop-blur sticky top-0 z-50 font-sans h-13">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-between h-16">

      <!-- Logo -->
      <div class="flex items-center z-50">
        <img class="h-8 w-auto" src={Logo} alt="Logo" />
        <span class="ml-3 text-xl font-semibold text-gray-900 dark:text-white">
          OMA <br>& Associates
        </span>
      </div>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex space-x-8">
        {#each navs as nav}
          <a 
            href={nav.href}
            class="text-lg font-semibold tracking-wide uppercase text-gray-900 dark:text-white hover:text-black dark:hover:text-gray-300 border-b-5 border-transparent hover:border-blue-800 dark:hover:border-white transition-colors duration-200 pb-1"
          >
            {nav.name}
          </a>
        {/each}
      </nav>

      <!-- Mobile toggle button -->
      <div class="md:hidden z-50">
        <button 
          on:click={() => mobileOpen = !mobileOpen}
          aria-expanded={mobileOpen}
          class="p-2 rounded-md text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-800 transition relative z-50"
        >
          <span class="sr-only">Open menu</span>
          {#if !mobileOpen}
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
            </svg>
          {:else}
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
            </svg>
          {/if}
        </button>
      </div>

    </div>
  </div>

  <!-- Mobile Sidebar -->
  <div
    class={`fixed inset-0 z-60 bg-white dark:bg-gray-900 flex flex-col items-center justify-center text-3xl font-semibold text-gray-900 dark:text-white transition-transform duration-300 h-13
      ${mobileOpen ? "translate-x-0 opacity-100" : "-translate-x-full opacity-0"}
    `}
    style:pointer-events={mobileOpen ? 'auto' : 'none'}
  >
    {#each navs as nav}
      <a href={nav.href} on:click={() => mobileOpen = false} class="hover:underline transition mb-8 last:mb-0">
        {nav.name}
      </a>
    {/each}
  </div>
</header>
