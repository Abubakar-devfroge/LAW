<script>
  let heading = "Annual Report 2025";
  let subheading = "Our latest report and letters to shareholders, released April 2025";
  let read = "Read the report";
  let src = '/wd.jpg';
</script>

<section 
  class="relative bg-cover bg-center bg-no-repeat h-[50vh] sm:h-[60vh] md:h-[70vh] lg:h-[80vh] rounded-none overflow-hidden mr-14 z-10"
  style="background-image: url({src});"
>

</section>


<section 
  class="relative bg-[#002147] text-white rounded-none  w-auto z-20 ml-20 h-[50vh] sm:h-[60vh] md:h-[70vh] lg:h-[80vh] 
         -mt-76 sm:-mt-84 md:-mt-90 lg:-mt-96"
>
  <div class="max-w-6xl mx-auto px-6 lg:px-12 py-12 sm:py-16 md:py-20 flex flex-col md:flex-row items-center justify-between gap-6">
    <div class="flex-1 flex flex-col md:flex-row md:items-center justify-between gap-4 w-full">
      

      <div class="max-w-2xl">
        <h2 class="text-3xl sm:text-3xl md:text-4xl lg:text-4xl font-semibold tracking-tight leading-tight mb-4">
          {heading}
        </h2>
        <p class="text-base sm:text-lg md:text-xl mb-6">
          {subheading}
        </p>
      </div>


      <div class="flex justify-start md:justify-end w-full md:w-auto">
        <a 
          href="/"
          class="relative inline-block px-8 py-3 text-sm sm:text-base md:text-base font-semibold tracking-wide uppercase 
                 before:absolute before:bottom-0 before:left-0 before:h-[5px] before:w-full 
                 before:bg-[#a82c30] before:origin-left before:scale-x-0 
                 before:transition-transform before:duration-300 before:ease-in-out
                 hover:before:scale-x-100"
        >
          {read}
        </a>
      </div>
    </div>
  </div>
</section>
