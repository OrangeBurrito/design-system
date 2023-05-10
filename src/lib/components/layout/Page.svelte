<script lang="ts">

</script>

<page-wrap>
    <page-header>
        <slot name="title"/>
        <slot name="description"/>
    </page-header>
    <slot/>
</page-wrap>

<style>
    page-wrap {
        display: block;
        flex-grow: 1;
        padding: var(--space-inset-3);
    }

    page-header {
        display: block;
        padding-bottom: var(--space-inset-3);
    }
</style>