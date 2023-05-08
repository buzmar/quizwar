<script>
	import { RadioActive } from 'radio-color-system';

	const nav = [
		{ icon: 'star', text: 'Trending' },
		{ icon: 'history', text: 'History' },
		{ icon: 'nightlife', text: 'Music' },
		{ icon: 'fastfood', text: 'Food' },
		{ icon: 'sports_basketball', text: 'Sports' },
		{ icon: 'sports_esports', text: 'Gaming' },
		{ icon: 'movie', text: 'Movies' }
	];
</script>

<navigation class=" primary-font-80">
	<a href="/" alt="Home" class="mdc-typography--headline2 primary-font-80"> QW </a>
	<ul>
		{#each nav as { icon, text }}
			<li>
				<a href={text} alt={text} class="primary-font-80">
					<span class="material-symbols-rounded icon"> {icon} </span>
					<span class="mdc-typography--subtitle1">{text}</span>
				</a>
			</li>
		{/each}
	</ul>
</navigation>
<div class="container">
	<h1 class="mdc-typography--headline2">Trending</h1>
	<div class="card-container">
		<RadioActive>
			<div class="card dynamic-80 dynamic-font-80">
				<img width="320" src="./images/capa.jpg" />
				<h2 class="mdc-typography--headline5">Anime who is stronger</h2>
				<p class="mdc-typography--body1">
					Material Design's text sizes and styles were developed to balance content density and
					reading comfort under typical usage conditions.
				</p>
			</div>
		</RadioActive>

		<RadioActive colors={[{ name: 'test' }]}>
			<div class="card test-80 test-font-80">
				<img class="test" width="320" src="./images/tile.png" />
				<h2 class="mdc-typography--headline5">Anime who is stronger</h2>
				<p class="mdc-typography--body1">
					Material Design's text sizes and styles were developed to balance content density and
					reading comfort under typical usage conditions.
				</p>
			</div>
		</RadioActive>

		<RadioActive colors={[{ name: 'mest' }]}>
			<div class="card mest-80 mest-font-80">
				<img width="320" src="./images/mantarus.jpeg" />
				<h2 class="mdc-typography--headline5">Anime who is stronger</h2>
				<p class="mdc-typography--body1">
					Material Design's text sizes and styles were developed to balance content density and
					reading comfort under typical usage conditions.
				</p>
			</div>
		</RadioActive>
	</div>
</div>

<style>
	.card-container {
		display: flex;
		gap: 2rem;
	}
	.container {
		width: 1240px;
		margin: 2rem auto;
	}
	navigation {
		display: flex;
		width: 1240px;
		margin: 2rem auto;
		padding: 1rem;
		border-radius: 0.5rem;
		justify-content: space-between;
	}
	ul {
		display: flex;
		flex-direction: row;
		list-style: none;
		padding: 0;
		margin: 0;
		gap: 0.5rem;
	}

	a {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 0.5rem 1rem;
		text-decoration: none;
	}

	.icon {
		font-size: 2rem;
		margin-bottom: 0.5rem;
	}

	.card {
		padding: 0 0 1rem 0;
		border-radius: 0.5rem;
		overflow: hidden;
		width: 320px;
	}
	.card h2,
	.card p {
		padding: 0 1rem;
	}

	.card img {
		box-shadow: 0 0 0 2px currentColor;
	}
</style>
