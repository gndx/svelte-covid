<script>
  export let global = {};
  export let countries = [];
</script>

<style>
  .Global {
    background-color: white;
    border-radius: 6px;
    border: 1px solid rgba(44,43,55, 0.2);
    padding: 1em 2em;
    margin: 1em 0;
  }
  .Global-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: center;
  }
  h2 {
    color: #D2161F;
  }
  .Global-item:nth-child(3n) h2 {
    color: #98ca3f;
  }
</style>

<div class="Global">
  <div class="Global-container">
    <div class="Global-content">
      <div class="Global-item">
        <h2>{countries.length}</h2>
        <span>Affected Countries</span>
      </div>
      <div class="Global-item">
        <h2>{global.TotalConfirmed}</h2>
        <span>Confirmed Cases</span>
      </div>
      <div class="Global-item">
        <h2>{global.TotalRecovered}</h2>
        <span>Recovered Cases</span>
      </div>
      <div class="Global-item">
        <h2>{global.TotalDeaths}</h2>
        <span>Worldwide Deaths</span>
      </div>
    </div>
  </div>
</div>