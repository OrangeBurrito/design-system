<script lang="ts">
    import Link from '$lib/components/text/Link.svelte'
</script>

<nav class="elevation-flat">
        <li>
        <Link href="/home">Home</Link>
        </li>
        <li>
        <Link href="/about">About</Link>
        </li>
        <li>
        <Link href="/contact">Contact</Link>
        </li>
</nav>

<style>
    nav {
        background-color: var(--color-layout-surface);
        padding: var(--space-inset-squish-2);
    }
</style>