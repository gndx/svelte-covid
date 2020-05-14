<script>
  import { onMount } from 'svelte';
  import Header from '../components/Header.svelte';
  import Global from '../components/Global.svelte';
  import Countries from '../components/Countries.svelte';
  import Footer from '../components/Footer.svelte';
  const API = 'https://api.covid19api.com/summary';
  let data = {};
  let error = false;

  onMount(async () => {
    try {
      const response = await fetch(API);
      data = await response.json();
    } catch (err) {
      error = true;
    }
  })
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');
  :global(body) {
    background-color: #f2f2f2;
    color: #2C2B37;
    font-family: 'Roboto', sans-serif;
  }
  .App {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }

</style>

<div class="App">
  <Header />
  {#if data.Global}
    <Global countries={data.Countries} global={data.Global} />
    <Countries countries={data.Countries} />
  {:else}
    <p>{error ? 'Lo sentimos ha ocurrido un error, Actualiza la pagina.' : 'Cargando...'}</p>
  {/if}
  <Footer />
</div>
