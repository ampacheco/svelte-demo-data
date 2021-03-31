<script>
	import Profile from "./Profile.svelte";
	import { onMount} from "svelte";
	
	let members = [];
	
	onMount( async() => {
			const res = await fetch(`https://raw.githubusercontent.com/ampacheco/svelte-demo-data/main/paypalmafia.json`);
			members = await res.json();
			console.log(members);
	});
	
</script>

<Profile>
	<span slot="name">Bob</span>
	<span slot="email">bob@email.com</span>
</Profile>

<Profile>
	<span slot="name">Alice</span>
	<span slot="phone">12345678</span>
</Profile>
