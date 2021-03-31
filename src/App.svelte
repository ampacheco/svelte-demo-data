<script>
	import { onMount } from 'svelte'
	import Profile from "./Profile.svelte";
	
	let members = [];
	
	onMount( async () => {
		const res = await fetch(`https://raw.githubusercontent.com/ampacheco/svelte-demo-data/main/paypalmafia.json`);
		members = await res.json();
		
		console.log(members);
	});
</script>

{#each members as member}
   <Profile name={member.name} title={member.title} mail={member.mail} />
{/each}
