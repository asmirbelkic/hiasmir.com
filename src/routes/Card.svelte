<script>
	import Tooltip from "./Tooltip.svelte";
	export let data;
</script>

<div>
<time>{data.date}</time>
<a href={data.link} target="_blank">
	<main>
		<h6>
				{#if data.image}
					<picture>{@html data.image}</picture>
				{/if}
				{data.title}
			</h6>
			{#if data.link}
				<div class="dot"></div>
			{/if}
	</main>
</a>
</div>

<style>
	div {
		text-decoration: none;
		gap: 16px;
		display: grid;
		grid-template-columns: 25% auto;
	}
	a:hover main {
		background: #f5f4f4;
	}
	div h6 {
		font-weight: 500;
		line-height: 1.2;
		display: flex;
		align-items: center;

		gap: .5rem;
		font-size: 1rem;
		font-weight: 600;
		color: #000;
	}
	div time {
		padding-top: 1rem;
		font-weight: 400;
		color: #737373;
	}
	div a {
		text-decoration: none;
	}
	div main picture {
		width: 1rem;
		height: 1rem;
		border-radius: 50%;
		overflow: hidden;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	div main .dot {
		width: 0.5rem;
    height: 0.5rem;
    background-color: #d6d6d6;
    border-radius: 50%;
		position: relative;
    flex: none;
    justify-content: center;
    align-items: center;
    display: flex;
	}
	div main {
		padding: 1rem 1.25rem;
		display: flex;
		align-items: center;
		justify-content: space-between;
		transition: background-color .2s;
		border-radius: 0.5rem;
		gap: 1rem;
	}
</style>
