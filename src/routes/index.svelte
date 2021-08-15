<script>
	import Nav from '../components/Nav.svelte';
	import CodeCard from '../components/CodeCard.svelte';
	import CheckoutProject from '../components/CheckoutProject.svelte';
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<Nav />
<div class="container">
	<p class="title">Brilliant Djaka I.R</p>
	<div class="subtitle">
		<p style="padding-right: 10px;">Backend</p>
		<p style="color: #869ACE;">Dev</p>
	</div>
	<div class="row">
		<CodeCard />
		<CheckoutProject />
	</div>
</div>

<style>
	* {
		margin: 0;
		padding: 0;
	}
	.title {
		text-align: center;
		font-size: 64px;
		font-family: 'Roboto', sans-serif;
		font-weight: 100;
		margin-bottom: 10px;
		margin-top: 30px;
	}
	.subtitle {
		margin-top: 11px;
		text-align: center;
		display: flex;
		justify-content: center;
		font-size: 48px;
		font-family: 'Roboto', sans-serif;
		font-weight: 100;
	}
	.container {
		display: grid;
		justify-content: center;
	}
	.row {
		display: flex;
	}
</style>
