<script lang="ts">
	import Breadcrumb from "../navigation/Breadcrumb.svelte"

    export let type: 'default' | 'home' | 'master-detail' | 'empty' = 'default'
    export let title = ''
    export let description = ''
    export let breadcrumb = true
</script>

<svelte:head>
    <title>{title}</title>
    <meta name="description" content={description}>
</svelte:head>

<page-wrap>
    <slot name="sidebar" />
    <body-wrap>
        <page-header>
            {#if breadcrumb}
            <Breadcrumb/>
            {/if}
            <h1>{title}</h1>
            <p>{description}</p>
        </page-header>
        <main>
            <slot />
        </main>
    </body-wrap>
</page-wrap>

<style>
	page-wrap {
		display: flex;
		flex-grow: 1;
	}

    body-wrap {
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        overflow: auto;
        scroll-behavior: smooth;
    }
    
	page-header {
        display: block;
        padding: var(--space-inset-3);
	}

    page-header :global(h1) { margin: 0; }
    
    main {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        padding: var(--space-inset-3);
    }
</style>
