<script>
	import Nav from '../components/Nav.svelte';
</script>

<Nav />
<div class="container">
	<p class="title">Credit</p>
	<a
		href="https://www.flaticon.com/free-icon/github_733609?term=github&page=1&position=13&page=1&position=13&related_id=733609&origin=search"
		>Github Logo</a
	>
	<a href="https://www.flaticon.com/free-icon/linkedin-logo_61109?term=linkedin&page=1&position=11"
		>Linkedin Logo</a
	>
	<a
		href="https://www.flaticon.com/free-icon/medium_2111505?term=medium&page=1&position=1&page=1&position=1&related_id=2111505&origin=search"
		>Medium Logo</a
	>
	<a
		href="https://www.flaticon.com/free-icon/instagram_2111463?term=instagram&page=1&position=2&page=1&position=2&related_id=2111463&origin=search"
		>Instagram Logo</a
	>
	<a
		href="https://www.flaticon.com/free-icon/gmail_732200?term=email&page=1&position=6&page=1&position=6&related_id=732200&origin=search"
		>Gmail Logo</a
	>
</div>

<style>
	a {
		color: black;
		padding: 10px;
	}
	.container {
		margin: 0 69px;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.title {
		text-align: center;
		font-size: 64px;
		font-family: 'Roboto', sans-serif;
		font-weight: 100;
		margin-bottom: 70px;
		margin-top: 30px;
		color: #869ace;
	}
</style>
