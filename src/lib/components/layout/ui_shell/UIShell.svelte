<script lang="ts">
    import Header from '$lib/components/layout/ui_shell/Header.svelte';
    import Sidebar from '$lib/components/layout/ui_shell/Sidebar.svelte';
</script>

<ui-shell>
    <Header/>
    <!-- <Sidebar/> -->
    <page-content>
        <slot/>
    </page-content>
</ui-shell>

<style>
    ui-shell {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    page-content {
        display: flex;
		flex-grow: 1;
		overflow-y: auto;
    }
</style>