<!----------- script special  ki permet de se jouer serveur et client ---->
<script context="module"> 
export async function preload(page, session){
 return { State: page.params["state"] }
}
</script>

<!------------------------------------------------- script normal  ---->

<script>

 import CovidStat from "../components/CovidStat.svelte"
	import CovidChart from "../components/CovidChart.svelte"

export let state
</script>

<!----------------------------------------------------------- HTML  ---->

<h1>{state}</h1>
<CovidStat />
<CovidChart />