<script>
	let darkMode = false;
	function toggle() {
        darkMode = !darkMode;
        window.document.body.classList.toggle('dark');
    }
</script>

<button on:click={toggle}>
	{#if darkMode }
		Go light
	{:else}
		Go dark
	{/if}
</button>

<style>
	button {
		border: 2px solid var(--text-color);
		border-radius: 5px;
		color: white;
        background:#8334eb;
		padding: 10px 15px;
	}
    button:active {
		background: inherit;
	}

	
</style>
