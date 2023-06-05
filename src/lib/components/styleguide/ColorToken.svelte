<script lang="ts">
    export let color = ''
    export let title = ''
    export let description = ''
</script>

<color-token>
    <div class="color" style={`background-color: ${color}`}></div>
    <h4>{title}</h4>
    <figcaption>{description}</figcaption>
</color-token>

<style>
    .color {
        width: 48px;
        height: 48px;
        border: 1px solid var(--color-border);
        margin-bottom: 0.5rem;
    }
</style>