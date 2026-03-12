<script lang="ts">
	const phases = [
		{
			date: 'Spring 2026',
			phase: 'Phase 1',
			title: 'Prototyping & Market Research',
			description: 'Deploy at schools, transit hubs, and festivals. Develop the brand and understand the community.',
			active: true
		},
		{
			date: 'Spring 2027',
			phase: 'Phase 2',
			title: 'Mobile Activation & Revenue Testing',
			description: 'Deploy the mobile bookcart. Revenue testing and building a loyal customer base.'
		},
		{
			date: 'Winter 2027',
			phase: 'Partnerships',
			title: 'Institutional Partnerships',
			description: 'Formalize partnerships with JPAC, schools, libraries, and cultural organizations.'
		},
		{
			date: '2028',
			phase: 'Phase 3',
			title: 'Brick-and-Mortar Storefront',
			description: 'Open the bookstore in downtown Jamaica, Queens — a retail destination and community hub.'
		},
		{
			date: 'Post 2028',
			phase: 'Expansion',
			title: 'Publishing & Beyond',
			description: 'Grow into publishing, media, education, and scale to immigrant-rich neighborhoods across NYC and global cities.'
		}
	];
</script>

<section class="py-24 bg-white">
	<div class="max-w-6xl mx-auto px-6">
		<div class="mb-16 text-center">
			<h2 class="text-4xl md:text-5xl font-bold text-gray-900">Intentionally Growing</h2>
			<p class="mt-4 text-lg text-gray-500 max-w-2xl mx-auto">
				A deliberate, phased approach to building something that lasts.
			</p>
		</div>

		<!-- Timeline -->
		<div class="relative">
			<!-- Horizontal line (desktop) -->
			<div class="hidden lg:block absolute top-16 left-0 right-0 h-0.5 bg-gray-200"></div>

			<div class="grid grid-cols-1 lg:grid-cols-5 gap-8">
				{#each phases as phase, i}
					<div class="relative flex flex-col items-center text-center group">
						<!-- Circle -->
						<div class="relative z-10 w-10 h-10 rounded-full border-2 flex items-center justify-center mb-4 transition-all
							{phase.active ? 'border-orange-500 bg-orange-500' : 'border-gray-300 bg-white group-hover:border-orange-400'}">
							{#if phase.active}
								<div class="w-3 h-3 bg-white rounded-full"></div>
							{:else}
								<div class="w-2 h-2 rounded-full bg-gray-300 group-hover:bg-orange-400 transition-colors"></div>
							{/if}
						</div>

						<!-- Date -->
						<div class="text-sm font-bold mb-1 {phase.active ? 'text-orange-500' : 'text-gray-400 group-hover:text-orange-400 transition-colors'}">
							{phase.date}
						</div>

						<!-- Phase badge -->
						<div class="text-xs font-bold uppercase tracking-wider text-gray-400 mb-2">{phase.phase}</div>

						<!-- Title -->
						<h3 class="font-bold text-gray-900 mb-2 text-sm leading-tight">{phase.title}</h3>

						<!-- Description -->
						<p class="text-xs text-gray-500 leading-relaxed uppercase tracking-wide">{phase.description}</p>

						{#if phase.active}
							<span class="mt-3 text-xs bg-orange-100 text-orange-700 px-2 py-0.5 rounded-full font-medium">
								Current Phase ★ Funding
							</span>
						{/if}
					</div>
				{/each}
			</div>
		</div>

		<!-- Future vision card -->
		<div class="mt-16 p-8 rounded-2xl bg-gray-900 text-white">
			<h3 class="text-xl font-bold mb-4">The bookstore is just the beginning.</h3>
			<div class="grid grid-cols-2 md:grid-cols-5 gap-4">
				{#each [
					{ icon: '📚', label: 'Publishing', desc: 'Amplify immigrant & diaspora authors' },
					{ icon: '🎙️', label: 'Media', desc: 'Podcasts, digital magazines, storytelling' },
					{ icon: '🎁', label: 'Lifestyle', desc: 'Gifts, apparel, branded merchandise' },
					{ icon: '🎓', label: 'Education', desc: 'Lecture series, language learning' },
					{ icon: '🌍', label: 'Expansion', desc: 'Scale to global diaspora cities' }
				] as item}
					<div class="text-center p-4 rounded-xl bg-white/10 hover:bg-white/20 transition-colors">
						<div class="text-2xl mb-2">{item.icon}</div>
						<div class="font-semibold text-sm mb-1">{item.label}</div>
						<div class="text-xs text-white/60">{item.desc}</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
