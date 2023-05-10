<script lang="ts">
	import Label from "./Label.svelte";

    export let label = ''
    export let placeholder = ''
</script>

<div class="input">
    <Label>{label}</Label>
    <input type="text" {placeholder}>
</div>

<style>
    input {
        padding: var(--space-inset-squish-1);
        border: var(--border-1);
    }

    input:focus {
        outline: var(--border-focus);
    }
</style>