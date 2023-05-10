<script lang="ts">
	import Icon from "$lib/components/content/Icon.svelte";

    export let type: 'primary' | 'secondary' | 'ghost' = 'primary'
    export let icon = ''
</script>

<button class={type} on:click>
    {#if icon}
        <Icon src={icon}/>
    {/if}
    <slot/>
</button>

<style>
    button {
        width: fit-content;
        display: flex;
        align-items: center;
        gap: var(--space-inline-1);
        padding: var(--space-inset-squish-1);

        --color-button-background: var(--color-background);
        --color-button-background-hover: var(--color-background-hover);
        --color-button-text: var(--color-text);

        background: var(--color-button-background);
        color: var(--color-button-text);
    }

    button:hover {
        background: var(--color-button-background-hover);
    }

    .primary {
        --color-button-background: var(--color-background-selected);
        --color-button-text: var(--color-text-inverted);
    }

    .primary:hover { --color-button-background-hover: var(--color-background-selected-hover) }

    .secondary {
        --color-button-background: var(--color-background-dark);
    }

    .ghost {
        --color-button-background: none;
        --color-button-text: var(--color-text-link);
    }
</style>