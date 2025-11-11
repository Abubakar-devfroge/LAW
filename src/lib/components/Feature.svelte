<script>
    let serve ="Serving with purpose";
    let paragraph = "We provide trusted, forward-thinking legal solutions for individuals, creators, and institutions. Combining precision and innovation, we help you protect what matters most.";
    let contact = "Contact Us";
    let img = "/law.webp";
    let alt = "Law Firm Office";
</script>



<section class="relative bg-white overflow-hidden py-8 md:py-16">
  <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center px-6 lg:px-12 gap-12 md:gap-20">
     <div class="flex-1 relative w-full h-[200px] md:h-[500px] rounded-none overflow-hidden ">
      <img 
        src={img} 
        {alt} 
        class="w-full h-auto object-cover transform hover:scale-105 transition-transform duration-700 ease-in-out"
      />
      <!-- <div class="absolute inset-0 bg-gradient-to-l from-white/0 to-white/70 md:to-white/60"></div> -->
    </div>

    <!-- Left: Text Content -->
    <div class="flex-1 text-left">
      <h2 class=" sm:text-5xl md:text-4xl font-bold text-gray-900 ">
      {serve}
      </h2>
      <p class=" sm:text-xl text-gray-600 mb-8 max-w-lg mt-2">
        {paragraph}
      </p>
    <a 
      href='#'
      class="text-lg font-semibold tracking-wide uppercase text-gray-900 dark:text-white hover:text-black dark:hover:text-gray-300 border-b-5 border-blue-800 hover:border-transparent dark:hover:border-white transition-colors duration-200 pb-1"
    >
       {contact}
      </a>
    </div>

    <!-- Right: Image -->
   

  </div>
</section>



