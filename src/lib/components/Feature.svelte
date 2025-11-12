<script>
    let serve ="Serving with purpose";
    let paragraph = "We provide trusted, forward-thinking legal solutions for individuals, creators, and institutions. Combining precision and innovation, we help you protect what matters most.";
    let contact = "Contact Us";
    let img = "/law.webp";
    let alt = "Law Firm Office";
</script>



<section class="relative bg-white overflow-hidden py-8 md:py-16">
  <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center px-6 lg:px-12 gap-12 md:gap-20">
     <div class="flex-1 relative w-full h-[200px] md:h-[500px] rounded-2xl overflow-hidden ">
      <img 
        src={img} 
        {alt} 
        class="w-full h-auto object-cover transform hover:scale-105 transition-transform duration-700 ease-in-out"
      />

    </div>


    <div class="flex-1 text-left">
      <h2 class=" sm:text-5xl md:text-4xl font-bold text-gray-900 ">
      {serve}
      </h2>
      <p class=" sm:text-xl text-gray-600 mb-8 max-w-lg mt-2">
        {paragraph}
      </p>
          <a 
            href="/"
            class="relative inline-block text-base rounded-2xl bg-gray-200 font-semibold text-gray-600 px-8 py-2
                   "
          >
            {contact}
          </a>

    </div>


   

  </div>
</section>



