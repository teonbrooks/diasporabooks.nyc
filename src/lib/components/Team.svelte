<script lang="ts">
	const team = [
		{
			name: 'Kion Sawney',
			role: 'Founder / CEO',
			image: null,
			initials: 'KS',
			bio: 'Visionary founder driving the mission to bring culturally-centered bookstores to underserved communities.'
		},
		{
			name: 'Teon Brooks',
			role: 'Founder / COO',
			image: null,
			initials: 'TB',
			bio: 'Co-founder leading operations, technology, and community partnerships to build Diaspora Books from the ground up.'
		}
	];

	const openRoles = [
		{ role: 'Activation Manager', description: 'Lead community activations, pop-up events, and mobile bookcart operations.' },
		{ role: 'Lead Book Buyer', description: 'Curate our collection with an eye for diaspora, immigrant, and multicultural voices.' }
	];
</script>

<section id="team" class="py-24 bg-white">
	<div class="max-w-6xl mx-auto px-6">
		<div class="mb-16 text-center">
			<h2 class="text-4xl md:text-5xl font-bold text-gray-900">Meet the Team</h2>
			<p class="mt-4 text-lg text-gray-500 max-w-2xl mx-auto">
				Built by community members, for the community.
			</p>
		</div>

		<!-- Founders -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-2xl mx-auto mb-12">
			{#each team as member}
				<div class="group p-6 rounded-2xl border border-gray-100 hover:border-orange-200 hover:shadow-lg transition-all text-center">
					<!-- Avatar -->
					<div class="w-24 h-24 rounded-2xl mx-auto mb-4 flex items-center justify-center text-2xl font-bold text-white gradient-brand shadow-md">
						{member.initials}
					</div>
					<h3 class="text-xl font-bold text-gray-900">{member.name}</h3>
					<p class="text-sm font-semibold uppercase tracking-wider text-orange-500 mt-1 mb-3">{member.role}</p>
					<p class="text-sm text-gray-500 leading-relaxed">{member.bio}</p>
				</div>
			{/each}
		</div>

		<!-- Now Hiring -->
		<div class="mt-4">
			<h3 class="text-center text-lg font-semibold text-gray-400 uppercase tracking-widest mb-8">Now Hiring</h3>
			<div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-2xl mx-auto">
				{#each openRoles as role}
					<div class="p-6 rounded-2xl border-2 border-dashed border-gray-200 hover:border-orange-300 transition-colors text-center group">
						<div class="w-24 h-24 rounded-2xl mx-auto mb-4 flex items-center justify-center text-3xl bg-gray-100 group-hover:bg-orange-50 transition-colors">
							👤
						</div>
						<h4 class="font-bold text-gray-900 mb-2">{role.role}</h4>
						<p class="text-sm text-gray-500 mb-4">{role.description}</p>
						<a
							href="mailto:hello@diasporabooks.nyc"
							class="inline-block text-sm font-semibold text-orange-600 hover:text-orange-700 underline underline-offset-2"
						>
							Apply →
						</a>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
