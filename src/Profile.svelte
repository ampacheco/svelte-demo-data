<script>
	export let name;
	export let title=null;
	export let mail;
	
</script>

<style>
	section {
		width: 350px;
		display: grid;
		grid-template-columns: 1fr 1fr;
		padding: 16px;
		box-shadow: 2px 2px 4px #dedede;
		border: 1px solid #888;
		margin-bottom: 16px;
	}
</style>

<section>
	<div>Name</div>
	<div>{name}</div>
	{#if title}
	<div>Title</div>
	<div>{title}</div>
	{/if}
	<div>Email</div>
	<div>{mail}@paypal@mafia</div>
</section>
