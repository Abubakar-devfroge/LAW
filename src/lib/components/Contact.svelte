<script>
  let heading = "Consulting and more";
  let subheading = "Contact us through : info@example.com.";
  let img = "/clip.webp";
</script>

<section class="relative bg-[#16473f] text-white py-12 md:py-20 overflow-hidden rounded-none mx-20">
  <div class="max-w-6xl mx-auto px-6 lg:px-12 flex flex-col md:flex-row items-center justify-between gap-6">

    <div class="flex-1 flex flex-col md:flex-row md:items-center justify-between gap-4 w-full">

    
      <div class="max-w-2xl">
        <h2 class="text-3xl md:text-4xl font-semibold tracking-tight leading-tight mb-4">
          {heading}
        </h2>
        <p class="sm:text-xl mb-6">
          {subheading}
        </p>


        <button class="bg-white text-gray-900 rounded-none text-xl font-medium py-2 px-4">Contact Form</button>
      </div>

     
      <div class="flex justify-start md:justify-end w-full md:w-auto">
        <img
          src="{img}"
          alt="Consulting"
          class="w-full h-auto md:w-auto md:h-40 object-cover  "
        />
      </div>

    </div>
  </div>
</section>
