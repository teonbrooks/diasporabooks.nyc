<section id="mission" class="py-24 relative overflow-hidden">
	<!-- Gradient background -->
	<div class="absolute inset-0 gradient-brand opacity-85"></div>

	<div class="relative z-10 max-w-4xl mx-auto px-6 text-center text-white">
		<div class="text-5xl mb-6">🌺</div>
		<h2 class="text-4xl md:text-6xl font-bold mb-6 leading-tight" style="font-family: 'Playfair Display', serif;">
			Diaspora Books
		</h2>
		<p class="text-xl md:text-2xl leading-relaxed text-white/90 max-w-3xl mx-auto">
			A community bookstore rooted in the stories of the world. We believe that by understanding different cultures and perspectives, we come to better understand ourselves.
		</p>

		<div class="mt-12 flex flex-wrap justify-center gap-4">
			{#each ['Black Diasporic Voices', 'South-Asian Stories', 'Immigrant Narratives', 'Community Gathering', 'Cultural Preservation'] as tag}
				<span class="px-4 py-2 bg-white/20 backdrop-blur-sm border border-white/30 rounded-full text-sm font-medium">
					{tag}
				</span>
			{/each}
		</div>
	</div>
</section>
