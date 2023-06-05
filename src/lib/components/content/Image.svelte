<script lang="ts">
    export let src = ''
    export let alt = ''
    export let caption = ''
</script>

<figure>
    <img {src} {alt}>
    <figcaption>{caption}</figcaption>
</figure>

<style>
    img {
        max-width: 400px;
        margin-bottom: var(--space-stack-1);
    }
</style>