<script lang="ts">
	import { page } from "$app/stores"

    let breadcrumbs = $page.route.id ? $page.route.id.split('/') : []
    breadcrumbs.shift()
    breadcrumbs.pop()
    breadcrumbs = breadcrumbs.map((link,i) => breadcrumbs.slice(0,i+1).join('/'))
</script>

<div class="breadcrumbs">
    {#each breadcrumbs as breadcrumb}
        <a class="breadcrumb" href={`/${breadcrumb}`}>{breadcrumb}</a>
    {/each}
</div>

<style>
    .breadcrumb:not(:last-of-type)::after {
        content: '/';
        color: var(--color-text-subtle);
        margin: 0 var(--space-inline-1);
    }
</style>