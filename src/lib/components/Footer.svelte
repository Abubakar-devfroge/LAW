<script>
  const footerLinks = [
    {
      title: "Company",
      links: [
        { name: "About Us", href: "#" },
        { name: "Leadership", href: "#" },
        { name: "Careers", href: "#" },
        { name: "News & Media", href: "#" },
      ],
    },
    {
      title: "Services",
      links: [
        { name: "Corporate Law", href: "#" },
        { name: "Intellectual Property", href: "#" },
        { name: "Litigation", href: "#" },
        { name: "Regulatory Compliance", href: "#" },
        { name: "Real Estate & Property", href: "#" },
      ],
    },
    {
      title: "Resources",
      links: [
        { name: "Annual Reports", href: "#" },
        { name: "Case Studies", href: "#" },
        { name: "Legal Insights", href: "#" },
        { name: "Contact Us", href: "#" },
      ],
    },
  ];
</script>

<footer class="bg-white text-gray-900">
  <div class="max-w-7xl mx-auto px-6 lg:px-12 py-12">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">

      {#each footerLinks as section}
        <div>
          <h3 class="text-lg font-semibold mb-4">{section.title}</h3>
          <ul class="space-y-2">
            {#each section.links as link}
              <li>
                        <a 
            href={link.href}
            class="relative inline-block border-b-2 border-transparent
                  before:absolute before:bottom-0 before:left-0 before:h-0.5 before:w-full 
                  before:bg-[#E29C20] before:origin-left before:scale-x-0
                  before:transition-transform before:duration-300 before:ease-in-out
                  hover:before:scale-x-100"
          >
            {link.name}
          </a>

              </li>
            {/each}
          </ul>
        </div>
      {/each}

    </div>

  
    <div class="mt-12 border-t border-gray-200 pt-6 text-center text-sm text-gray-500">
      &copy; {new Date().getFullYear()} OMA & Associates. All rights reserved.
    </div>
  </div>
</footer>
