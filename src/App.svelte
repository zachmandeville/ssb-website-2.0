<script>
	import { Router, Route } from "svelte-routing";
	import NavLink from "./components/NavLink.svelte"
	import Home from "./routes/Home.svelte";
	import Values from "./routes/Values.svelte";
	import About from "./routes/About.svelte";

// Used for SSR. A falsy value is ignored by the Router.
export let url = "";
</script>

<Router url="{url}">
	<nav>
		<NavLink to="/">Home</NavLink>
		<NavLink to="values">Values</NavLink>
		<NavLink to="about">About</NavLink>
	</nav>
	<div>
		<Route path="about" component="{About}" />
		<Route path="values" component="{Values}" />
		<Route path="/" component="{Home}" />
	</div>
</Router>




