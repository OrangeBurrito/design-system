<script lang="ts">
    export let title = ''
</script>

<nav>
    <h3 id={title}>{title}</h3>
    <slot/>
</nav>

<style>
    nav {
        display: flex;
        flex-direction: column;
    }
</style>