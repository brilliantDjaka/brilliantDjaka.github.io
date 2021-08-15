<script>
	import Nav from '../components/Nav.svelte';
	import { datas, categories } from '../../static/content.json';
	let selected = '';
</script>

<svelte:head>
	<title>Projects</title>
</svelte:head>

<Nav />
<div class="container">
	<p class="title">
		Projects <span style="color: #CA3D3D;">Page</span>
	</p>

	<div class="row">
		<p style="margin-right: 5px;">Category :</p>
		<select bind:value={selected}>
			<option selected value="">All</option>
			{#each categories as category}
				<option value={category}>{category}</option>
			{/each}
		</select>
	</div>
	{#each datas as data}
		{#if !selected || data.category.includes(selected)}
			<a class="content" href={data.url}>
				<img src={data.imageUrl} alt={data.title} width="324" height="155" />
				<div class="sub-content">
					<div class="row">
						<p class="sub-title">{data.title}</p>
						<a style="width: min-content; max-height: min-content;" href={data.sourceCode}
							><div class="git" /></a
						>
					</div>

					<p>{data.description}</p>
				</div>
			</a>
		{/if}
	{/each}
</div>

<style>
	.git {
		background-image: url('/github.svg');
		background-size: contain;
		height: 28px;
		width: 28px;
	}
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
		font-family: 'Roboto', sans-serif;
		font-size: 36px;
		font-weight: 300;
		margin-right: 10px;
	}
	.row {
		display: flex;
		align-items: center;
		margin-bottom: 20px;
	}
	select {
		background-color: white;
		border: 1px solid black;
		border-radius: 5px;
		height: 30px;
		width: 200px;
	}
</style>
