<script>
    import Button from './components/Button.svelte'
    import ToggleMode from './components/Toggle-Mode.svelte'
    import Matrix from './components/Matrix.svelte'
</script>

<main>
    <h1>Svelte Components</h1>
    <ul>
        <li><h3>Ripple Effect Button</h3><Button/></li>
        <li><h3>Dark-Light Mode Toggle</h3><ToggleMode/></li>
        <li><h3>Matrix Rain</h3><Matrix/></li>
    </ul>
</main>

<style>
	main {
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

    :global(body.dark){
        background-color:black;
        color:white;
    }

	h1 {
        text-align: center;
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
