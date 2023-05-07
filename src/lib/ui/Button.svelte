<script lang="ts">
	export let text = '';
	export let onClick: (() => void) | undefined = undefined;
	export let varient: 'primary' | 'secondary' = 'primary';
	export let size: 'sm' | 'md' = 'md';
	export let href: string | undefined = undefined;
</script>

{#if href}
	<a {href} class={`${varient} ${size}`}>{text}</a>
{:else}
	<button on:click={onClick} class={`${varient} ${size} `}>{text}</button>
{/if}

<style lang="postcss">
	button,
	a {
		@apply text-center inline-flex capitalize transition-all duration-500 border-0 focus:outline-none  rounded;
	}
	.sm {
		@apply py-1 px-3 text-base;
	}
	.md {
		@apply py-2 px-6 text-lg;
	}
	.primary {
		@apply text-white bg-blue-500 hover:bg-blue-600;
	}
	.secondary {
		@apply text-gray-700 bg-gray-100 hover:bg-gray-200;
	}
</style>
