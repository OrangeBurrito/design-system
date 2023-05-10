<script lang="ts">
    import '../styles/reset.css'
    import '../styles/global.css'

	import PageHeader from '$lib/components/layout/PageHeader.svelte';
	import SideNav from '$lib/components/layout/SideNav.svelte';
</script>

<PageHeader/>
<page-content>
    <SideNav/>
    <slot/>
</page-content>

<style>
    page-content {
        height: 100%;
        display: flex;
    }
</style>