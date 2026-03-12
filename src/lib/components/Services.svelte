<script lang="ts">
	import { Book, Package, Calendar, Star } from 'lucide-svelte';

	const services = [
		{
			icon: Book,
			title: 'Books',
			badge: '70% of inventory',
			description: 'New books, magazines, and periodicals focused on literary fiction, nonfiction, and children\'s books — centering Black and South-Asian diasporic voices.',
			color: 'blue'
		},
		{
			icon: Package,
			title: 'Nonbooks & Merchandise',
			badge: '30% of inventory',
			description: 'Vinyl, stationery, greeting cards, and culturally relevant gifts to diversify revenue and create accessible entry points.',
			color: 'orange'
		},
		{
			icon: Calendar,
			title: 'Events',
			badge: 'Community',
			description: 'Author talks, workshops, book festivals, and cultural programming that bring the neighborhood together.',
			color: 'purple'
		},
		{
			icon: Star,
			title: 'Memberships',
			badge: 'Coming Soon',
			description: 'Discounts, exclusive book clubs, early access to events, and a deeper connection to the Diaspora Books community.',
			color: 'green'
		}
	];

	const colorMap: Record<string, string> = {
		blue: 'bg-blue-100 text-blue-600',
		orange: 'bg-orange-100 text-orange-600',
		purple: 'bg-purple-100 text-purple-600',
		green: 'bg-green-100 text-green-600'
	};

	const badgeColorMap: Record<string, string> = {
		blue: 'bg-blue-50 text-blue-700',
		orange: 'bg-orange-50 text-orange-700',
		purple: 'bg-purple-50 text-purple-700',
		green: 'bg-green-50 text-green-700'
	};
</script>

<section id="services" class="py-24 bg-gray-50">
	<div class="max-w-6xl mx-auto px-6">
		<div class="mb-16">
			<h2 class="text-4xl md:text-5xl font-bold text-gray-900">Products & Services</h2>
			<p class="mt-4 text-lg text-gray-500 max-w-2xl">
				More than just books — a destination for culture, community, and connection.
			</p>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			{#each services as service}
				{@const Icon = service.icon}
				<div class="bg-white rounded-2xl p-8 border border-gray-100 hover:shadow-lg transition-all hover:-translate-y-0.5 group">
					<div class="flex items-start justify-between mb-4">
						<div class="w-12 h-12 rounded-xl flex items-center justify-center {colorMap[service.color]}">
							<Icon size={22} />
						</div>
						<span class="text-xs font-semibold px-3 py-1 rounded-full {badgeColorMap[service.color]}">
							{service.badge}
						</span>
					</div>
					<h3 class="text-xl font-bold text-gray-900 mb-2 group-hover:text-orange-600 transition-colors">{service.title}</h3>
					<p class="text-gray-600 leading-relaxed">{service.description}</p>
				</div>
			{/each}
		</div>

		<!-- Shop CTA -->
		<div class="mt-12 text-center">
			<p class="text-gray-500 mb-4">Browse our current online collection</p>
			<a
				href="https://bookshop.org/shop/diasporabooks_nyc"
				target="_blank"
				rel="noopener noreferrer"
				class="inline-flex items-center gap-2 px-8 py-4 rounded-full font-semibold text-white text-lg transition-all hover:opacity-90 hover:shadow-lg hover:-translate-y-0.5"
				style="background: linear-gradient(135deg, #4A86C8, #E8921A);"
			>
				<Book size={20} />
				Shop on Bookshop.org
			</a>
		</div>
	</div>
</section>
