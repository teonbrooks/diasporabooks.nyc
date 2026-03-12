<script lang="ts">
	import { BookOpen, ArrowRight } from 'lucide-svelte';
</script>

<section class="py-24 relative overflow-hidden">
	<div class="absolute inset-0 gradient-brand opacity-90"></div>

	<div class="relative z-10 max-w-4xl mx-auto px-6 text-center text-white">
		<div class="inline-flex items-center gap-2 bg-white/20 border border-white/30 rounded-full px-4 py-2 text-sm font-medium mb-8">
			<span class="w-2 h-2 bg-white rounded-full animate-pulse"></span>
			Coming soon to Queens · Spring 2026
		</div>

		<h2 class="text-4xl md:text-6xl font-bold mb-6 leading-tight" style="font-family: 'Playfair Display', serif;">
			Bloom Everywhere
		</h2>

		<p class="text-xl text-white/80 max-w-2xl mx-auto mb-10 leading-relaxed">
			Follow our journey as we bring a culturally-rooted bookstore to Southeast Queens. Shop our collection online while we build toward opening day.
		</p>

		<div class="flex flex-col sm:flex-row gap-4 justify-center">
			<a
				href="https://bookshop.org/shop/diasporabooks_nyc"
				target="_blank"
				rel="noopener noreferrer"
				class="flex items-center justify-center gap-2 bg-white text-gray-900 px-8 py-4 rounded-full font-semibold text-lg hover:bg-orange-50 transition-all hover:shadow-xl hover:-translate-y-0.5"
			>
				<BookOpen size={20} />
				Shop Now on Bookshop.org
				<ArrowRight size={18} />
			</a>
			<a
				href="mailto:hello@diasporabooks.nyc"
				class="flex items-center justify-center gap-2 bg-white/20 backdrop-blur-sm border border-white/40 text-white px-8 py-4 rounded-full font-semibold text-lg hover:bg-white/30 transition-all"
			>
				Get in Touch
			</a>
		</div>

		<p class="mt-8 text-white/50 text-sm">
			diasporabooks.nyc · Downtown Jamaica, Queens, NYC
		</p>
	</div>
</section>
