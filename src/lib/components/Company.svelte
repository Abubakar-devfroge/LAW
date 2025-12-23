<script>
  let heading = "Company Details";
  let Details = "We are located at 123 Business St, Suite 456, Metropolis. Our phone number is (123) 456-7890.";
  let subheading = "Contact us through : info@example.com.";
  let img = "/clip.webp";
</script>

<section class="relative bg-background text-gray-900 py-12 md:py-20 overflow-hidden rounded-none mx-20 ">
  <div class="max-w-6xl mx-auto px-6 lg:px-12 flex flex-col md:flex-row items-center justify-between gap-6">

    <div class="flex-1 flex flex-col md:flex-row md:items-center justify-between gap-4 w-full">

      <!-- Text -->
      <div class="max-w-2xl">
         <h2 class="text-3xl md:text-4xl font-semibold tracking-tight leading-tight mb-4">
          {heading}
        </h2>
        <h4 class="text-xl md:text-xl font-semibold tracking-tight leading-tight mb-4">
          {Details}
        </h4>
        <p class="sm:text-xl mb-6">
          {subheading}
        </p>


        <button class="bg-white text-gray-900 rounded-none text-xl font-medium py-2 px-4">Contact Form</button>
      </div>

      <!-- Image (same visual weight as button) -->
      <div class="flex justify-start md:justify-end w-full md:w-auto">
      {Details}
      </div>

    </div>
  </div>
</section>
