<script lang="ts">
    export let title = ''
    export let id = ''
</script>

<section>
    <h2 class="title" {id}>{title}</h2>
    <slot/>
</section>

<style>
    section .title {
        margin-top: 0;
    }
</style>