<script>
	export let name;
	let animate;
</script>

<main>
	<h1 class="{animate ? `animate` : ''}">Hello {name}!</h1>
	<label>
		<input type=checkbox bind:checked={animate}>
		Animate
	</label>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

h1 {
	margin: 0;
	font-size: 20vw;
	position: relative;
	font-weight: 400;
	font-family: 'Decovar';
	/* font-family: 'Montserrat'; */
	/* font-family: 'AmstelvarAlpha'; */

	/* // Background clip to image */
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
	background-image: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/209981/209708058_b5a5fb07a6_o.jpg);
	background-size: 30%;
	background-repeat: repeat;

	text-shadow: 2px 2px 5px rgba(#2a4308, 0.4);
}

.animate {
  animation: grow 2s infinite alternate-reverse;
}

 @keyframes grow {
	0% {
		font-variation-settings: 'wght' 10, 'wdht' 10, 'slnt' 10, 'INLN' 10, 'SWRM' 0;
	}

	100% {
		font-variation-settings: 'wght' 0, 'wdht' 1500, 'slnt' 1500, 'INLN' 500, 'SWRM' 1000;
	}
}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
