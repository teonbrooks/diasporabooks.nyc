<script lang="ts">
	import { ArrowRight, BookOpen } from 'lucide-svelte';
</script>

<section class="relative min-h-screen flex items-center justify-center overflow-hidden">
	<!-- Gradient background -->
	<div class="absolute inset-0 gradient-brand opacity-90"></div>

	<!-- Subtle pattern overlay -->
	<div class="absolute inset-0 opacity-10 pattern-dots"></div>

	<div class="relative z-10 max-w-4xl mx-auto px-6 text-center text-white">
		<!-- Badge -->
		<div class="inline-flex items-center gap-2 bg-white/20 backdrop-blur-sm border border-white/30 rounded-full px-4 py-2 text-sm font-medium mb-8">
			<span class="w-2 h-2 bg-white rounded-full animate-pulse"></span>
			Coming to Queens · Spring 2026
		</div>

		<!-- Main headline -->
		<h1 class="text-6xl md:text-8xl font-bold mb-4 leading-tight" style="font-family: 'Playfair Display', serif;">
			Diaspora Books
		</h1>

		<!-- Tagline -->
		<p class="text-2xl md:text-3xl font-light mb-6 text-white/90 italic" style="font-family: 'Playfair Display', serif;">
			Bloom Everywhere
		</p>

		<!-- Description -->
		<p class="text-lg md:text-xl text-white/80 max-w-2xl mx-auto mb-10 leading-relaxed">
			A community bookstore rooted in the stories of the world. By understanding different cultures and perspectives, we come to better understand ourselves.
		</p>

		<!-- CTAs -->
		<div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
			<a
				href="https://bookshop.org/shop/diasporabooks_nyc"
				target="_blank"
				rel="noopener noreferrer"
				class="flex items-center gap-2 bg-white text-gray-900 px-8 py-4 rounded-full font-semibold text-lg hover:bg-orange-50 transition-all hover:shadow-xl hover:-translate-y-0.5"
			>
				<BookOpen size={20} />
				Shop Our Collection
				<ArrowRight size={18} />
			</a>
			<a
				href="#about"
				class="flex items-center gap-2 bg-white/20 backdrop-blur-sm border border-white/40 text-white px-8 py-4 rounded-full font-semibold text-lg hover:bg-white/30 transition-all"
			>
				Our Story
			</a>
		</div>

		<!-- Location -->
		<p class="mt-12 text-white/60 text-sm font-medium tracking-widest uppercase">
			Downtown Jamaica · Queens, NYC
		</p>
	</div>

	<!-- Scroll indicator -->
	<div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-white/50 animate-bounce">
		<span class="text-xs tracking-widest uppercase">Scroll</span>
		<div class="w-px h-8 bg-white/30"></div>
	</div>
</section>
