<script lang="ts">
	let { targetDate } = $props();

	let days = $state(0);
	let hours = $state(0);
	let minutes = $state(0);
	let seconds = $state(0);
	let message = $state('');

	const interval = setInterval(() => {
		const now = new Date().getTime();
		const distance = targetDate.getTime() - now;

		if (distance < 0) {
			const hoursAfter = Math.abs(distance) / (1000 * 60 * 60);
			if (hoursAfter <= 4) {
				message = 'NOW OPEN';
			} else {
				message = '';
				clearInterval(interval);
			}
			days = 0;
			hours = 0;
			minutes = 0;
			seconds = 0;
			return;
		}

		days = Math.floor(distance / (1000 * 60 * 60 * 24));
		hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
		minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
		seconds = Math.floor((distance % (1000 * 60)) / 1000);
	}, 1000);
</script>

<div class="countdown-container">
	{#if message}
		<span class="message">{message}</span>
	{:else}
		<span class="timer">{days}d {hours}h {minutes}m {seconds}s</span>
	{/if}
</div>

<style>
	.countdown-container {
		position: fixed;
		top: 0;
		left: 50%;
		transform: translateX(-50%);
		padding: 1rem 2rem;
		background-color: var(--primary-color);
		border-radius: 0 0 10px 10px;
		z-index: 1000;
		text-align: center;
	}

	.timer,
	.message {
		font-size: 2.5rem;
		font-weight: bold;
		color: var(--light-color);
		text-shadow: 2px 2px 4px var(--primary-color);
		letter-spacing: 0.1em;
	}
</style>
