<script context="module">
    import requests from "../data/request.js";
    export async function preload() {
        try {
            const usStats = await requests.usStats();
            return {usStats}
        } catch(e) {

        }
    }
</script>

<script>
  import CovidStat from '../components/CovidStat.svelte';
  import CovidChart from '../components/CovidChart.svelte';
  import TableContainer from '../components/TableContainer.svelte';

  export let usStats;
  console.log(usStats);s
</script>

<svelte:head>
    <title>About Covide 19 Tracker US</title>
</svelte:head>

<div class="section header">
    <div class="container">
        <h1>Covid 19 - US</h1>
    </div>
</div>

<CovidStat />
<CovidChart />

<TableContainer />