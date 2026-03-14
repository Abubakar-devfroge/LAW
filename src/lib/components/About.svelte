<script>
	let Aboutheading = 'One of Kenya’s Premier Law Firms';
	let Aboutparagraph =
		'We are one of Kenya’s premier law firms, providing high-quality legal services to individuals, businesses, and institutions across the country. Our firm combines deep legal expertise with a practical understanding of the Kenyan regulatory and commercial landscape.';
	let img = '/sup.webp';
</script>

<section>
	<div class="mx-auto max-w-7xl px-4 py-8 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 gap-4 md:grid-cols-4 md:items-center md:gap-8">
			<div class="md:col-span-1">
				<div class="max-w-prose md:max-w-none">
					<h2 class="text-2xl font-semibold text-gray-900 sm:text-3xl">
						{Aboutheading}
					</h2>

					<p class="mt-4 text-pretty text-gray-700">
						{Aboutparagraph}
					</p>
				</div>
			</div>

			<div class="md:col-span-3">
				<img src={img} class="rounded" alt="About us" />
			</div>
		</div>
	</div>
</section>
