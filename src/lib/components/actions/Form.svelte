<script>
	import Stack from "../layout/Stack.svelte";
    export let title = ''
</script>

<form>
    <Stack>
        <h2>{title}</h2>
        <slot/>
    </Stack>
</form>