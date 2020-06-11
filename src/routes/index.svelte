<svelte:head>
	<title>tutturu!~</title>
</svelte:head>
<script>
    import Tutturu from '../components/Tutturu.svelte'
    import Search from '../components/Search.svelte'
    import Extensions from '../components/Extensions.svelte'
</script>

<main class="box">
    <Tutturu />
    <Search />
    <Extensions />
</main>

<style>
    .box {
        text-align: center;
        position: absolute;
        top: 60%;
        left: 50%;
        transform: translate(-50%, -60%);
    }
</style>
