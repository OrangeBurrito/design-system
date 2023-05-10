<script lang="ts">
    export let size: 1 | 2 | 3 | 4 = 1;
</script>

{#if size === 1}
    <h1><slot/></h1>
{:else if size === 2}
    <h2><slot/></h2>
{:else if size === 3}
    <h3><slot/></h3>
{:else if size === 4}
    <h4><slot/></h4>
{/if}