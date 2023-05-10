<script>
	import Icon from "../content/Icon.svelte";

</script>
<select>
    <slot/>
</select>

<style>
    select {
        -moz-appearance: none; /* Firefox */
        -webkit-appearance: none; /* Safari and Chrome */
        appearance: none;
        background-image: url('/icons/chevron-down.svg');
        background-repeat: no-repeat;
        background-position: center right;
        background-origin: content-box;

        padding: var(--space-inset-squish-1);
        border: var(--border-1);
    }

    select:focus {
        background-image: url('/icons/chevron-up.svg')
    }
</style>