<script lang="ts">
	import { Menu, X } from 'lucide-svelte';

	let mobileOpen = $state(false);

	const navLinks = [
		{ label: 'About', href: '#about' },
		{ label: 'Shop', href: '#shop' },
		{ label: 'Events', href: '#services' },
		{ label: 'Our Story', href: '#mission' },
		{ label: 'Team', href: '#team' }
	];
</script>

<nav class="fixed top-0 left-0 right-0 z-50 bg-white/90 backdrop-blur-md border-b border-gray-100 shadow-sm">
	<div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
		<!-- Logo -->
		<a href="/" class="flex items-center gap-2">
			<span class="text-2xl">🌺</span>
			<span class="font-bold text-gray-900" style="font-family: 'Playfair Display', serif;">Diaspora Books</span>
		</a>

		<!-- Desktop nav -->
		<div class="hidden md:flex items-center gap-8">
			{#each navLinks as link}
				<a
					href={link.href}
					class="text-sm font-medium text-gray-600 hover:text-orange-500 transition-colors"
				>
					{link.label}
				</a>
			{/each}
		</div>

		<!-- CTA -->
		<div class="hidden md:flex items-center gap-3">
			<a
				href="https://bookshop.org/shop/diasporabooks_nyc"
				target="_blank"
				rel="noopener noreferrer"
				class="px-5 py-2 rounded-full text-sm font-semibold text-white transition-all hover:opacity-90 hover:shadow-md"
				style="background: linear-gradient(135deg, #4A86C8, #E8921A);"
			>
				Shop Now
			</a>
		</div>

		<!-- Mobile menu toggle -->
		<button
			class="md:hidden p-2 rounded-lg text-gray-600 hover:bg-gray-100"
			onclick={() => mobileOpen = !mobileOpen}
			aria-label="Toggle menu"
		>
			{#if mobileOpen}
				<X size={20} />
			{:else}
				<Menu size={20} />
			{/if}
		</button>
	</div>

	<!-- Mobile menu -->
	{#if mobileOpen}
		<div class="md:hidden bg-white border-t border-gray-100 px-6 py-4 flex flex-col gap-4">
			{#each navLinks as link}
				<a
					href={link.href}
					class="text-sm font-medium text-gray-700 hover:text-orange-500"
					onclick={() => mobileOpen = false}
				>
					{link.label}
				</a>
			{/each}
			<a
				href="https://bookshop.org/shop/diasporabooks_nyc"
				target="_blank"
				rel="noopener noreferrer"
				class="mt-2 px-5 py-2 rounded-full text-sm font-semibold text-white text-center"
				style="background: linear-gradient(135deg, #4A86C8, #E8921A);"
				onclick={() => mobileOpen = false}
			>
				Shop Now
			</a>
		</div>
	{/if}
</nav>
