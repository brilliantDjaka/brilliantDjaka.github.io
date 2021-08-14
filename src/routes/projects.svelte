<script>
	import Nav from '../components/Nav.svelte';
	import { datas, category } from '../../static/content.json';
</script>

<Nav />
<div class="container">
	<p class="title">
		Projects <span style="color: #CA3D3D;">Page</span>
	</p>
	{#each datas as data}
		<a class="content" href={data.url}>
			<img src={data.imageUrl} alt={data.title} width="324" height="155" />
			<div class="sub-content">
				<p class="sub-title">{data.title}</p>
				<p>{data.description}</p>
			</div>
		</a>
	{/each}
</div>

<style>
	img {
		margin-right: 25px;
		border: 1px solid black;
	}
	* {
		margin: 0;
		padding: 0;
	}
	.title {
		text-align: center;
		font-size: 64px;
		font-family: 'Roboto', sans-serif;
		font-weight: 100;
		margin-bottom: 50px;
		margin-top: 30px;
	}
	.container {
		margin: 0 69px;
	}
	.content {
		text-decoration: none;
		color: black;
		display: flex;
		margin-bottom: 42px;
	}
	.sub-content {
		max-width: 600px;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	p {
		font-family: 'Roboto', sans-serif;
		font-weight: 300;
		font-size: 18px;
	}
	.sub-title {
		margin-bottom: 20px;
		font-family: 'Roboto', sans-serif;
		font-size: 36px;
		font-weight: 300;
	}
</style>
