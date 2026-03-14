<script>
	let active = 0;

	const areas = [
		{
			id: 1,
			title: 'Corporate & Commercial Law',
			desc: 'Advising companies on structuring, governance, regulatory compliance, and major commercial transactions.',
			img: 'https://images.unsplash.com/photo-1450101499163-c8848c66ca85?auto=format&fit=crop&q=80&w=1200'
		},
		{
			id: 2,
			title: 'Dispute Resolution & Litigation',
			desc: 'Representation in complex commercial disputes, arbitration proceedings, and court litigation.',
			img: 'https://images.unsplash.com/photo-1589829545856-d10d557cf95f?auto=format&fit=crop&q=80&w=1200'
		},
		{
			id: 3,
			title: 'Real Estate & Property Law',
			desc: 'Legal support for property development, land acquisition, leasing, and regulatory approvals.',
			img: 'https://images.unsplash.com/photo-1560518883-ce09059eeffa?auto=format&fit=crop&q=80&w=1200'
		},
		{
			id: 4,
			title: 'Employment & Labour Law',
			desc: 'Advising employers and executives on contracts, compliance, disputes, and workplace policies.',
			img: 'https://images.unsplash.com/photo-1551836022-d5d88e9218df?auto=format&fit=crop&q=80&w=1200'
		}
	];
</script>

<section class="bg-white py-20">
	<div class="mx-auto max-w-7xl px-6">
		<div class="grid gap-16 lg:grid-cols-2 items-center">
			<!-- LEFT VISUAL -->
			<div class="relative h-[420px] overflow-hidden rounded-2xl bg-gray-100">
				<img
					src={areas[active].img}
					class="absolute inset-0 h-full w-full object-cover transition duration-500"
					alt=""
				/>

				<div class="absolute inset-0 bg-black/40"></div>

				<div class="relative flex h-full flex-col justify-end p-10 text-white">
					<h3 class="mt-2 text-3xl font-semibold">
						{areas[active].title}
					</h3>

					<p class="mt-3 max-w-md text-gray-200 leading-relaxed">
						{areas[active].desc}
					</p>
				</div>
			</div>

			<!-- RIGHT CONTENT -->
			<div>
				<!-- SWITCHER -->
				<div class="mt-12 space-y-3">
					{#each areas as area, i (area.id)}
						<button
							on:click={() => (active = i)}
							class="group flex w-full items-center justify-between rounded-xl px-6 py-5 text-left transition
    {active === i ? 'bg-gray-100' : 'hover:bg-gray-100/70'}"
						>
							<span class="text-lg font-medium text-black">
								{area.title}
							</span>
						</button>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>
