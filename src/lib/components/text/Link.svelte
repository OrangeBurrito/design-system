<script lang="ts">
    export let href = ''
</script>

<a {href}><slot/></a>

<style>
    a, a:visited {
        color: var(--color-text-link);
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }
</style>