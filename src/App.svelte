<script>
    import Button from './components/Button.svelte'
    import ToggleMode from './components/Toggle-Mode.svelte'
    import Matrix from './components/Matrix.svelte'
    import Tabs from './components/Tabs.svelte'

    let items = ['Home', 'About'];
    let activeItem = 'Home';

    const tabChange = (e) => {
        activeItem = e.detail;
    }
</script>

<main>
    <h1>Svelte Components</h1>
    <Tabs {activeItem} {items} on:tabChange={tabChange} />
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

    ul{
        display: flex;
    }
    ul >li{
        padding-left:5%;
        list-style-type:none;
    }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
