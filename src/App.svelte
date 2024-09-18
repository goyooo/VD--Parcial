<script>
    import * as d3 from "d3"
  import Waffles from "./lib/Waffles.svelte"

  let numbers = [21, 33, 42, 54, 63, 71, 77, 84, 92, 98]
  let numbers1 = [23, 35, 45, 56, 50, 43, 38, 32, 28, 25]
  const years = [2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023]

</script>

<div class="header">
  <h2> El Legado de la Prevención</h2>
  <h4>La crisis de la gripe aviar en 2017 definió el destino de dos familias en su búsqueda por la victoria</h4>
</div>
 <div class="maples">

  <div class="blockazo1">
    <h3 class="title">Chapaleofú</h3>
    <div class="años">
      {#each years as y}
        <p class="año">{y}</p>
      {/each}
    </div>

    <Waffles
      numbers={numbers}
      title= "Chapaleofu"
    />

  </div>

  <div class="blockazo">
    <h3 class="title">Delgado</h3>
    <div class="años">
      {#each years as y}
        <p class="año">{y}</p>
      {/each}
    </div>

    <Waffles
    numbers={numbers1}
    title="Delgado"
    />
  </div>
</div>

<p class="titulo-de-graf"> Otras formas de ver los datos</p>
<div class="graficos-f">
  <div class="flourish-embed flourish-chart" data-src="visualisation/19448565"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/19448565/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  <div class="flourish-embed flourish-chart" data-src="visualisation/19448458"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/19448458/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
</div>


<style>
  .title{
    background-color: #498a49;
    color:#c0975a;
    text-align: center;
    text-decoration-thickness: 2px;
    font-size: 40px;
    font-family: 'Trebuchet MS';
    margin-bottom:0%;
  }
 .titulo-de-graf {
  text-align: center;
  text-decoration:underline;
  text-decoration-thickness: 2px;
  font-size: 25px;
  font-family: 'Trebuchet MS';
 }

  .graficos-f {
    display: flex;
    margin-bottom: 0%;
    margin-top: 5%
  }

  .flourish-embed  {
    width: 50%;
    height: 50%;
  }

  .header {
    font-family: 'Cochin';
    color: rgb(218, 215, 215);
    display: flex;
    flex-direction: column;
    text-align: center;
    background-color: rgb(73, 138, 73);
  }

  .años {
    display: flex;
    justify-content: space-around;
    background-color: #498a49;
    font-family:'Trebuchet MS';
    font-size: 27px;
    color: #c79d6b;
    margin-bottom: 0%   
  }

  .maples {
    margin-top: 0%;
    display: flex;
    flex-direction: column;
  }

</style>