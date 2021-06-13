<script>
		import { LottiePlayer } from '@lottiefiles/svelte-lottie-player';
</script>

<style>
	.wrapper {
		position: relative;
	}
	
	#lottie {
		animation: fadeIn 100s linear 14s;
		animation-delay: 0s;
		position: absolute;
	}
	
	.congrats {
		animation: fadeInCongrats 100s linear 14s;
		animation-delay: 0s;
		position: absolute;
		z-index:10;
	}
	
	@keyframes fadeIn {
  0% { opacity: 0; }
  20% { opacity: 0; }
  40% { opacity: 0; }
  60% { opacity: 0; }
  90% { opacity: 0.8; }
  100% { opacity: 1; }
}
	
	@keyframes fadeInCongrats {
  0% { opacity: 0; }
  20% { opacity: 0; }
  40% { opacity: 0; }
  60% { opacity: 0; }
  90% { opacity: 0.3; }
	98% { opacity: 0.5; }
  100% { opacity: 1; }
}
</style>

<div class="wrapper">
	<div id="lottie">
	<LottiePlayer
  src='https://assets7.lottiefiles.com/packages/lf20_kd7V2C.json'
  autoplay={true}
  loop={true}
  controls={false}
  renderer='svg'
  background='transparent'
  height={window.innerHeight}
  width={window.innerWidth}
  controlsLayout={[
		"previousFrame",
		"playpause",
		"stop",
		"nextFrame",
		"progress",
		"frame",
		"loop",
		"spacer",
		"background",
		"snapshot",
		"zoom",
		"info"
	]} />
</div>
<div class="congrats">
	<LottiePlayer
  src='https://assets10.lottiefiles.com/temporary_files/49MSGC.json'
  autoplay={true}
  loop={true}
  controls={false}
  renderer='svg'
  background='transparent'
  height="{1600}"
  width="{1200}"
  controlsLayout={[
		"previousFrame",
		"playpause",
		"stop",
		"nextFrame",
		"progress",
		"frame",
		"loop",
		"spacer",
		"background",
		"snapshot",
		"zoom",
		"info"
	]} />
</div>
</div>