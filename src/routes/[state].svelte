<script context="module"> 
    export async function preload(page) {
        console.log(page)
        return { state: page.params['state']}
    }
</script>
<script>
    import CovidStat from '../components/CovidStat.svelte';
    import CovidChart from '../components/CovidChart.svelte';
    import TableContainer from '../components/TableContainer.svelte';
    export let state;
</script>
<svelte:head>
    <title>About Covide 19 Tracker US</title>
</svelte:head>

<div class="section header">
    <div class="container">
        <h1>Covid 19 - US</h1>
    </div>
</div>

<h1>{state}</h1>
<CovidStat />
<CovidChart />