<script lang="ts">
    import Header from '$lib/components/ui_shell/Header.svelte';
    import Sidebar from '$lib/components/ui_shell/Sidebar.svelte';
</script>

<ui-shell>
    <Header/>
    <Sidebar/>
    <slot/>
</ui-shell>