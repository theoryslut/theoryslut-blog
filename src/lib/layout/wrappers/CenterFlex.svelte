<script>
	export let figure = false;
	export let figcaption = '';
	export let added_class = '';
</script>

{#if figure}
	<figure class="center-flex {added_class}">
		<slot />
		<figcaption class="caption">{figcaption}</figcaption>
	</figure>
{:else}
	<div class="center-flex {added_class}">
		<slot />
	</div>
{/if}

<style>
	figure {
		margin: 0;
		padding: 0;
	}

	.image {
		max-height: 700px;
		max-width: 90%;
	}
	.caption {
		max-width: 70%;
	}

	.center-flex {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
</style>
