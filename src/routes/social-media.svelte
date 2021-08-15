<script>
	import Nav from '../components/Nav.svelte';
	import { userData } from '../../static/content.json';
</script>

<svelte:head>
	<title>Social Media</title>
</svelte:head>

<Nav />
<div class="container">
	<p class="title">
		<span style="color: #CA3D3D;">Social</span> <span style="color: #869ACE;">Media</span>
	</p>
	<div style="display: flex; flex-direction: column; align-items: center;">
		<div>
			{#each userData as { name, src, href, alt }}
				<a {href} class="menu">
					<img width="28px" height="28px" {src} {alt} />
					<p>{name}</p>
				</a>
			{/each}
		</div>
	</div>
</div>

<style>
	a {
		text-decoration: none;
	}
	p {
		margin: 0;
		padding: 3px 0 0 0;
	}
	.menu {
		display: flex;
		color: #606060;
		margin-bottom: 19px;
	}
	img {
		margin-right: 12px;
	}
	.container {
		margin: 0 69px;
	}
	.title {
		text-align: center;
		font-size: 64px;
		font-family: 'Roboto', sans-serif;
		font-weight: 100;
		margin-bottom: 70px;
		margin-top: 30px;
	}
</style>
