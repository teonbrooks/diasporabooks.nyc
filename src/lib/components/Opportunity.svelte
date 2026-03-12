<script lang="ts">
	const opportunities = [
		{
			number: '01',
			title: 'Unmatched Diversity',
			description: 'Queens is the most diverse county in America with over 1.5 million immigrants and 160+ languages spoken.'
		},
		{
			number: '02',
			title: 'Population Growth',
			description: 'The Jamaica Neighborhood Plan will bring over 12,000 new housing units, making it one of NYC\'s fastest-growing residential centers.'
		},
		{
			number: '03',
			title: 'Transit Gateway',
			description: 'Downtown Jamaica is a major hub with direct access to the LIRR, seven subway lines, 50+ bus routes, and the AirTrain to JFK — serving 60M+ travelers yearly.'
		},
		{
			number: '04',
			title: 'Market Gap',
			description: 'Millions of potential readers are being underserved, representing a significant and untapped market opportunity.'
		}
	];
</script>

<section class="py-24 bg-white">
	<div class="max-w-6xl mx-auto px-6">
		<div class="mb-16 text-center">
			<h2 class="text-4xl md:text-5xl font-bold text-gray-900">The Opportunity</h2>
			<p class="mt-4 text-lg text-gray-500 max-w-2xl mx-auto">
				Everything points to Queens as the right place, at the right time.
			</p>
		</div>

		<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each opportunities as opp}
				<div class="group p-6 rounded-2xl border border-gray-100 hover:border-orange-200 hover:shadow-lg transition-all hover:-translate-y-1">
					<div class="text-sm font-bold text-gray-300 mb-3 tracking-widest">{opp.number}</div>
					<h3 class="text-lg font-bold text-gray-900 mb-3 group-hover:text-orange-600 transition-colors">
						{opp.title}
					</h3>
					<p class="text-sm text-gray-500 leading-relaxed uppercase tracking-wide">{opp.description}</p>
				</div>
			{/each}
		</div>

		<!-- Stats bar -->
		<div class="mt-16 grid grid-cols-2 md:grid-cols-4 gap-6">
			{#each [
				{ stat: '1.5M+', label: 'Immigrants in Queens' },
				{ stat: '160+', label: 'Languages Spoken' },
				{ stat: '12,000', label: 'New Housing Units' },
				{ stat: '60M+', label: 'JFK Travelers/Year' }
			] as item}
				<div class="text-center p-6 rounded-2xl bg-gradient-to-br from-blue-50 to-orange-50">
					<div class="text-3xl font-bold gradient-brand-text mb-1">{item.stat}</div>
					<div class="text-sm text-gray-500">{item.label}</div>
				</div>
			{/each}
		</div>
	</div>
</section>
