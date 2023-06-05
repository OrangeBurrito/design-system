<script lang="ts">
	// import { page } from "$app/stores";

    // const routes = import.meta.glob('/src/routes/**/*.svelte')

    // import('src/routes/**/*.svelte')

    // console.log(routes)
</script>

<div class="sidebar">
    <slot/>
</div>

<style>
    .sidebar {
        width: 200px;
        padding: var(--space-inset-2);
        background: var(--color-background-alt);
    }
</style>