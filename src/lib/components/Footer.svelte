<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="bg-gray-900 text-white py-16">
	<div class="max-w-6xl mx-auto px-6">
		<div class="grid grid-cols-1 md:grid-cols-4 gap-10 mb-12">
			<!-- Brand -->
			<div class="md:col-span-2">
				<div class="flex items-center gap-2 mb-4">
					<span class="text-2xl">🌺</span>
					<span class="text-xl font-bold" style="font-family: 'Playfair Display', serif;">Diaspora Books</span>
				</div>
				<p class="text-gray-400 text-sm leading-relaxed max-w-xs">
					A community bookstore rooted in the stories of the world. Bloom Everywhere.
				</p>
				<div class="mt-4 flex items-center gap-2">
					<span class="w-2 h-2 bg-orange-500 rounded-full animate-pulse"></span>
					<span class="text-sm text-gray-400">Coming Spring 2026 · Downtown Jamaica, Queens</span>
				</div>
			</div>

			<!-- Links -->
			<div>
				<h4 class="font-semibold mb-4 text-sm uppercase tracking-widest text-gray-400">Navigate</h4>
				<ul class="space-y-2">
					{#each [
						{ label: 'Our Mission', href: '#mission' },
						{ label: 'Products & Services', href: '#services' },
						{ label: 'Our Roadmap', href: '#roadmap' },
						{ label: 'The Team', href: '#team' }
					] as link}
						<li>
							<a href={link.href} class="text-sm text-gray-400 hover:text-orange-400 transition-colors">{link.label}</a>
						</li>
					{/each}
				</ul>
			</div>

			<!-- Shop & Contact -->
			<div>
				<h4 class="font-semibold mb-4 text-sm uppercase tracking-widest text-gray-400">Shop & Connect</h4>
				<ul class="space-y-2">
					<li>
						<a
							href="https://bookshop.org/shop/diasporabooks_nyc"
							target="_blank"
							rel="noopener noreferrer"
							class="text-sm text-orange-400 hover:text-orange-300 transition-colors font-medium"
						>
							Shop on Bookshop.org ↗
						</a>
					</li>
					<li>
						<a href="mailto:hello@diasporabooks.nyc" class="text-sm text-gray-400 hover:text-white transition-colors">
							hello@diasporabooks.nyc
						</a>
					</li>
					<li>
						<span class="text-sm text-gray-500">Downtown Jamaica, Queens, NYC</span>
					</li>
				</ul>
			</div>
		</div>

		<div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center gap-4 text-xs text-gray-500">
			<p>© {currentYear} Diaspora Books NYC. All rights reserved.</p>
			<p class="text-center">
				Supporting independent bookstores via
				<a href="https://bookshop.org" target="_blank" rel="noopener noreferrer" class="text-orange-400 hover:text-orange-300 transition-colors">Bookshop.org</a>
			</p>
		</div>
	</div>
</footer>
