<script>
	import Star from './star.svelte';
	import Intro from './Intro.svelte';
	import Logo from './logo.svelte';
	import Scroll from './scroll.svelte';
	import End from './end.svelte';
	import { onMount } from 'svelte';
	let muted = false;
	let paused = false;
	let randomStars = 257;
	let stars = [];
	const getRandomXYPos = () => {
		const x = window.innerWidth;
		const y = window.innerHeight;
		const randomX = Math.floor(Math.random()*x);
		const randomY = Math.floor(Math.random()*y);
		console.log(randomX, randomY, x, y)
		return [randomX, randomY];
	};

	const drawStars = () => {
		let starInfo = [];
		for(let i=0; i<randomStars; i++) {
			let [x,y] = getRandomXYPos();
			starInfo.push({x, y});
		}
		return starInfo;
	}

	onMount(async () => {
		stars = drawStars();
	});
</script>

<style>
	:global(body) {
		background-color: #000;
		color: #bfc2c7;
	}
</style>

<!-- svelte-ignore a11y-media-has-caption -->
<audio preload="auto" autoplay bind:muted={muted} bind:paused={paused}>
  <source src="/music/intro.mp3" type="audio/mpeg">
</audio>

<Intro/>
<Logo/>
<Scroll/>
<End/>

{#each stars as star}
	<Star {...star}></Star>
{/each}

