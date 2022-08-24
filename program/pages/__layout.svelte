<script>
	import '@program/program.css';
	import NavBar from '@program/components/navbar.svelte';
	import Footer from '@program/components/footer.svelte';
</script>

<div>
	<NavBar />
	<slot />
	<Footer />
</div>
