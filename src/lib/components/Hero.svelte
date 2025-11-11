<script>
  let heading = "Legal ";
  let heading2 = "Excellence";
  let subheading = "Personalized for You";
  let src = '/sup.webp';
  import '../../app.css';
</script>

<section class="relative min-h-[70vh] md:min-h-[80vh] flex items-start md:items-center bg-black overflow-hidden rounded-none ">
  <div class="absolute inset-0">
    <img src={src} alt="Hero background" class="w-full h-full object-cover"/>
    <!-- <div class="absolute inset-0 bg-linear-to-r from-black/40 via-black/20 to-black/70"></div> -->
  </div>


  <div class="relative z-10 max-w-7xl  px-6 flex flex-col md:flex-row items-start md:items-center justify-between h-full pt-32 md:pt-40">
    

    <div class="text-left max-w-xl md:max-w-2xl flex flex-col justify-start md:justify-center h-full">
      <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-extrabold text-white mb-6 opacity-0 animate-fade-in-down">
        {heading}
        <br />
        {heading2}
      </h1>
      <p class="text-lg sm:text-xl md:text-2xl text-white mb-6 opacity-0 animate-fade-in-down animation-delay-200">
       {subheading}
      </p>
      
    </div>

       <!-- <div class="flex justify-start  md:justify-end items-start md:items-center h-full m-1 md:mt-0 opacity-0 animate-fade-in-down animation-delay-400">
      <a href="/Login" 
         class="px-6 py-1 bg-white text-black font-normal rounded-none text-lg hover:bg-gray-200 transition">
        Contact us
      </a>
    </div> -->
  </div>
 
</section>

<style>
  @keyframes fadeInDown {
    0% { opacity: 0; transform: translateY(-20px); }
    100% { opacity: 1; transform: translateY(0); }
  }

  .animate-fade-in-down {
    animation: fadeInDown 0.6s forwards;
  }
  .animation-delay-200 {
    animation-delay: 0.2s;
  }
</style>
