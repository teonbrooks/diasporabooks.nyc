<section id="shop" class="py-24 bg-white">
	<div class="max-w-6xl mx-auto px-6">
		<div class="rounded-3xl overflow-hidden border border-gray-100 shadow-xl">
			<div class="gradient-brand p-1">
				<div class="bg-white rounded-2xl">
					<!-- Header -->
					<div class="p-8 border-b border-gray-100 flex flex-col md:flex-row items-start md:items-center justify-between gap-4">
						<div>
							<div class="flex items-center gap-2 mb-2">
								<span class="text-2xl">🌺</span>
								<span class="font-bold text-gray-900 text-lg" style="font-family: 'Playfair Display', serif;">Diaspora Books</span>
								<span class="text-xs bg-orange-100 text-orange-700 px-2 py-0.5 rounded-full font-medium">on Bookshop.org</span>
							</div>
							<p class="text-gray-500 text-sm">
								Shop our curated selection of books celebrating diaspora, immigrant, and multicultural voices.
							</p>
						</div>
						<a
							href="https://bookshop.org/shop/diasporabooks_nyc"
							target="_blank"
							rel="noopener noreferrer"
							class="flex-shrink-0 px-6 py-3 rounded-full text-white font-semibold text-sm transition-all hover:opacity-90 hover:shadow-md"
							style="background: linear-gradient(135deg, #4A86C8, #E8921A);"
						>
							Visit Full Store →
						</a>
					</div>

					<!-- Featured categories -->
					<div class="p-8 grid grid-cols-1 sm:grid-cols-3 gap-4">
						{#each [
							{ emoji: '✊🏾', title: 'Black Diasporic Voices', desc: 'Fiction, nonfiction & poetry centering Black stories from around the world' },
							{ emoji: '🌏', title: 'South-Asian Stories', desc: 'Literature and narratives from South Asia and its global diaspora' },
							{ emoji: '👧🏽', title: "Children's Books", desc: 'Diverse books that reflect every child\'s heritage and imagination' }
						] as cat}
							<div class="p-5 bg-gradient-to-br from-orange-50 to-blue-50 rounded-xl text-center hover:shadow-md transition-all hover:-translate-y-0.5 cursor-pointer group">
								<div class="text-3xl mb-3">{cat.emoji}</div>
								<h4 class="font-bold text-gray-900 mb-2 group-hover:text-orange-600 transition-colors">{cat.title}</h4>
								<p class="text-xs text-gray-500 leading-relaxed">{cat.desc}</p>
							</div>
						{/each}
					</div>

					<!-- Bookshop.org affiliate note -->
					<div class="px-8 pb-6 text-center">
						<p class="text-xs text-gray-400">
							We partner with <strong>Bookshop.org</strong> — every purchase supports independent bookstores and our community mission.
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
