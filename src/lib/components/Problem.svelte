<script lang="ts">
	import { BookX, Users, MapPin, TrendingDown } from 'lucide-svelte';

	const problems = [
		{
			icon: BookX,
			title: 'Book Desert',
			description: 'Queens has less than half the bookstores of Brooklyn, leaving Southeast Queens severely underserved.'
		},
		{
			icon: Users,
			title: 'Limited Representation',
			description: 'Immigrant families lack access to books that reflect their stories, languages, and heritage.'
		},
		{
			icon: MapPin,
			title: 'Few Third Spaces',
			description: 'Downtown Jamaica lacks consistent community gathering spaces for residents to connect and grow.'
		},
		{
			icon: TrendingDown,
			title: 'Economic Leakage',
			description: 'Consumer spending flows out of the neighborhood due to unmet demand for services, goods, and values.'
		}
	];
</script>

<section id="about" class="py-24 bg-gray-50">
	<div class="max-w-6xl mx-auto px-6">
		<!-- Label -->
		<div class="mb-12">
			<span class="text-sm font-bold tracking-widest uppercase" style="color: #7B4FC9;">As of Today</span>
			<h2 class="mt-3 text-4xl md:text-5xl font-bold text-gray-900 leading-tight">
				Southeast Queens deserves better.
			</h2>
			<p class="mt-4 text-lg text-gray-500 max-w-2xl">
				The community faces real challenges that a culturally-grounded bookstore can help solve.
			</p>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-2 gap-px bg-gray-200 rounded-2xl overflow-hidden shadow-sm">
			{#each problems as problem}
				{@const Icon = problem.icon}
				<div class="bg-white p-8 hover:bg-orange-50/30 transition-colors group">
					<div class="flex items-start gap-4">
						<div class="flex-shrink-0 w-12 h-12 rounded-xl flex items-center justify-center bg-orange-100 group-hover:bg-orange-200 transition-colors">
							<Icon size={22} class="text-orange-600" />
						</div>
						<div>
							<h3 class="text-xl font-bold text-gray-900 mb-2">{problem.title}</h3>
							<p class="text-gray-600 leading-relaxed">{problem.description}</p>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
