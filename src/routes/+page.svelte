<script lang="ts">
	import Nav from '$lib/components/Nav.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Problem from '$lib/components/Problem.svelte';
	import Opportunity from '$lib/components/Opportunity.svelte';
	import Mission from '$lib/components/Mission.svelte';
	import Services from '$lib/components/Services.svelte';
	import Shop from '$lib/components/Shop.svelte';
	import Roadmap from '$lib/components/Roadmap.svelte';
	import Advantages from '$lib/components/Advantages.svelte';
	import Team from '$lib/components/Team.svelte';
	import CTA from '$lib/components/CTA.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
	<title>Diaspora Books NYC — Bloom Everywhere</title>
	<meta name="description" content="A community bookstore rooted in the stories of the world. Coming to Downtown Jamaica, Queens in Spring 2026. Celebrating Black and South-Asian diasporic voices." />
	<meta property="og:title" content="Diaspora Books NYC — Bloom Everywhere" />
	<meta property="og:description" content="A community bookstore rooted in the stories of the world. Coming to Downtown Jamaica, Queens in Spring 2026." />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://diasporabooks.nyc" />
</svelte:head>

<Nav />

<main>
	<Hero />
	<Problem />
	<Opportunity />
	<Mission />
	<Services />
	<Shop />
	<div id="roadmap">
		<Roadmap />
	</div>
	<Advantages />
	<Team />
	<CTA />
</main>

<Footer />
