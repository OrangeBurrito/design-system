<script lang="ts">
	import Breadcrumb from "$lib/components/navigation/Breadcrumb.svelte"

</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<Breadcrumb breadcrumbs={[{url: "/", title: "Home"}, {url: "/about", title: "About"}]}/>

<h2>About</h2>
