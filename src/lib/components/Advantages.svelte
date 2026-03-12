<script lang="ts">
	import { Trophy, Heart, Home, Handshake, TrendingUp } from 'lucide-svelte';

	const advantages = [
		{
			icon: Trophy,
			title: 'First-Mover in Queens',
			description: 'The only independent bookstore in Southeast Queens — serving a community long overlooked by mainstream retail.'
		},
		{
			icon: Heart,
			title: 'Culturally Curated',
			description: 'Immigrant and diaspora voices at the center — unlike Barnes & Noble and other chains that treat diversity as an afterthought.'
		},
		{
			icon: Home,
			title: 'Community Hub',
			description: 'A true "third space" where people gather, not just retail. Events, workshops, and belonging built into the model.'
		},
		{
			icon: Handshake,
			title: 'Partnership Model',
			description: 'Deep ties with schools, libraries, and arts organizations drive institutional revenue and community trust.'
		},
		{
			icon: TrendingUp,
			title: 'Scalable Vision',
			description: 'The model is replicable in immigrant-rich neighborhoods across NYC and global diaspora cities.'
		}
	];
</script>

<section class="py-24 bg-gray-50">
	<div class="max-w-6xl mx-auto px-6">
		<div class="grid md:grid-cols-2 gap-16 items-center">
			<!-- Left: content -->
			<div>
				<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Competitive Advantages</h2>
				<p class="text-lg text-gray-500 mb-8">
					We're not just filling a market gap — we're building something that can't be replicated by chains.
				</p>

				<div class="space-y-5">
					{#each advantages as adv}
						{@const Icon = adv.icon}
						<div class="flex items-start gap-4 group">
							<div class="flex-shrink-0 w-10 h-10 rounded-lg flex items-center justify-center bg-orange-100 group-hover:bg-orange-200 transition-colors mt-0.5">
								<Icon size={18} class="text-orange-600" />
							</div>
							<div>
								<h3 class="font-bold text-gray-900 mb-1">{adv.title}</h3>
								<p class="text-sm text-gray-500 leading-relaxed">{adv.description}</p>
							</div>
						</div>
					{/each}
				</div>
			</div>

			<!-- Right: visual -->
			<div class="rounded-2xl overflow-hidden shadow-xl">
				<div class="gradient-brand p-8 text-white">
					<div class="text-6xl mb-4">🌺</div>
					<blockquote class="text-xl font-medium leading-relaxed italic mb-4" style="font-family: 'Playfair Display', serif;">
						"Stories have always crossed borders. Now they have a home in Queens."
					</blockquote>
					<div class="mt-6 pt-6 border-t border-white/30 grid grid-cols-2 gap-4">
						{#each [
							{ label: 'Only independent', sub: 'bookstore in SE Queens' },
							{ label: 'Diaspora-first', sub: 'curation model' },
							{ label: '160+ languages', sub: 'in our community' },
							{ label: 'Scalable', sub: 'to global cities' }
						] as stat}
							<div class="bg-white/20 backdrop-blur-sm rounded-xl p-3 text-center">
								<div class="font-bold text-sm">{stat.label}</div>
								<div class="text-xs text-white/70 mt-0.5">{stat.sub}</div>
							</div>
						{/each}
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
