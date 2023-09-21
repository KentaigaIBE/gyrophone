<script lang="ts">
	import { browser } from '$app/environment';

	let alpha: number | null = 0;
	let beta: number | null = 0;
	let gamma: number | null = 0;

	if (browser) {
		window.addEventListener('deviceorientation', handleOrientation);

		function handleOrientation(event: DeviceOrientationEvent) {
			alpha = event.alpha;
			beta = event.beta;
			gamma = event.gamma;
		}
	}
</script>

<h1>Gryophone</h1>
<p>Use the power of your phone to get rotation data!</p>
<br />
<p>Alpha: {alpha}</p>
<p>Beta: {beta}</p>
<p>Gamma: {gamma}</p>
