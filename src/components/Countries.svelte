<script>
  import Country from './Country';
  import Search from './Search';
  export let countries = [];
  let searchCountries = countries;

  const handleSearch = (event) => {
    const value = event.target.value;
    searchCountries = countries.filter(country =>
      country.Country.toLowerCase().includes(value.toLowerCase())
    );
  }

</script>

<style>
  .Countries {
    background-color: white;
    border-radius: 6px;
    border: 1px solid rgba(44,43,55, 0.2);
    margin: 1em 0;
  }
  .Countries-header {
    display: grid;
    grid-template-columns: repeat(5,1fr);
    grid-gap: 1em;
    text-align: center;
  }
</style>

<Search handleSearch={handleSearch} />

<div class="Countries">
  <div class="Countries-header">
    <div>
      <h3>Pais</h3>
    </div>
    <div>
      <h3>Casos Nuevos</h3>
    </div>
    <div>
      <h3>Confirmados</h3>
    </div>
    <div>
      <h3>Recuperados</h3>
    </div>
    <div>
      <h3>Muertes</h3>
    </div>
  </div>
  <div class="Countries-items">
    {#each searchCountries as country}
      <Country country={country} />
    {/each}
  </div>
</div>