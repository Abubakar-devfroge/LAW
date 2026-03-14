<script>
	let heading = 'Strategic. Ethical. Exceptional.';
	let subheading =
		'Partnering with clients to deliver forward-thinking legal strategies, unmatched advocacy, and service defined by the highest professional standards.';
	let read = 'Request Legal Counsel';

	let heading2 = 'Personalized Legal Solutions';
	let subheading2 = 'Tailored legal services to meet your unique needs.';
	let read2 = 'Learn more';
</script>

<section class="relative bg-[#F7F3E8] text-black py-14 md:py-20 overflow-hidden mr-20">
	<div
		class="max-w-6xl mx-auto px-6 lg:px-12 flex flex-col md:flex-row md:items-center md:justify-between gap-10"
	>
		<!-- Text -->
		<div class="max-w-2xl">
			<h2 class="text-3xl md:text-4xl font-semibold tracking-tight leading-tight mb-4">
				{heading}
			</h2>

			<p class="sm:text-lg text-gray-700">
				{subheading}
			</p>
		</div>

		<!-- Button -->
		<div class="shrink-0">
			<a
				href="/contact"
				class="inline-block px-8 py-2 rounded-md text-sm md:text-base bg-[#245524] font-semibold tracking-wide uppercase text-white border-2 border-[#245524] hover:bg-transparent hover:text-[#245524] transition duration-300"
			>
				{read}
			</a>
		</div>
	</div>
</section>

<section class="relative bg-[#F7F3E8] text-black py-14 md:py-20 overflow-hidden ml-20 mb-14">
	<div
		class="max-w-6xl mx-auto px-6 lg:px-12 flex flex-col md:flex-row md:items-center md:justify-between gap-10"
	>
		<!-- Text -->
		<div class="max-w-2xl">
			<h2 class="text-3xl md:text-4xl font-semibold tracking-tight leading-tight mb-4">
				{heading2}
			</h2>

			<p class="sm:text-lg text-gray-700">
				{subheading2}
			</p>
		</div>

		<!-- Button -->
		<div class="shrink-0">
			<a
				href="/about"
				class="inline-block rounded-md px-8 py-2 text-sm md:text-base bg-[#245524] font-semibold tracking-wide uppercase text-white border-2 border-[#245524] hover:bg-transparent hover:text-[#245524] transition duration-300"
			>
				{read2}
			</a>
		</div>
	</div>

	<div
		class="absolute inset-x-0 bottom-0 h-16 bg-linear-to-t from-black/20 to-transparent pointer-events-none"
	></div>
</section>
