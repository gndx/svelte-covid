<script>
  export let country = {};
</script>

<style>
  .Country-items {
    display: grid;
    grid-template-columns: repeat(5,1fr);
    grid-gap: 1em;
    border-top: 1px solid rgba(44,43,55,0.2);
    text-align: center;
  }
  h3 {
    padding: 0 1em;
    color: rgba(44, 43, 55, 0.7);
    font-size: 16px;
  }
</style>

<div class="Country">
  <div class="Country-items">
    <div class="Country-item">
      <h3>{country.Country}</h3>
    </div>
    <div class="Country-item">
      <h3>{country.NewConfirmed}</h3>
    </div>
    <div class="Country-item">
      <h3>{country.TotalConfirmed}</h3>
    </div>
    <div class="Country-item">
      <h3>{country.TotalConfirmed}</h3>
    </div>
    <div class="Country-item">
      <h3>{country.TotalDeaths}</h3>
    </div>
  </div>
</div>