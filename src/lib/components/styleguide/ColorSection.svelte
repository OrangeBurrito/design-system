<script lang="ts">
    export let title = ''
</script>

<color-section>
    <h3>{title}</h3>
    <div class="colors">
        <slot/>
    </div>
</color-section>

<style>
    .colors {
        display: flex;
        gap: 1rem;
    }

    h3 {
        margin-bottom: 1rem;
    }
</style>