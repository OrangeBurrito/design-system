<script lang="ts">
    export let direction: 'row' | 'column' = 'column'
</script>

<div class="stack {direction}">
    <slot/>
</div>

<style>
    .stack {
        display: flex;
        gap: var(--space-inline-1);
    }
    
    .stack.column {
        flex-direction: column;
        gap: var(--space-stack-2);
    }
</style>