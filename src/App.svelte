<script>
    import * as d3 from "d3"
  import Waffles from "./lib/Waffles.svelte"
  import image3 from './src/images/huevo.png';
  let numbers = [21, 33, 42, 54, 63, 71, 77, 84, 92, 98]
  let numbers1 = [23, 35, 45, 56, 50, 43, 38, 32, 28, 25]
  const years = [2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023]

</script>
<img src={image3}
         alt=''
         >

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

    <div class="waffles_container">

      {#each numbers as n}
    
      <div class="waffle_wrapper">
        <p class="cant">{n}</p>
        <div class="waffle">
          
          {#each d3.range(0, 100) as number}
            {#if number < n}
              <div class="cuad lleno">
                <img class="buevito" src="./public/images/huevo.png" alt="buevito" style="transform: rotate(180deg);">
              </div>
            {:else}
              <div class="cuad vacio"></div>
            {/if}
          {/each}
        </div>
        
      </div>
    
      {/each}
    </div>

  </div>

  <div class="blockazo">
    <h3 class="title">Delgado</h3>
    <div class="años">
      {#each years as y}
        <p class="año">{y}</p>
      {/each}
    </div>

    <div class="waffles_container">

      {#each numbers as n}
    
      <div class="waffle_wrapper">
        <p class="cant">{n}</p>
        <div class="waffle">
          
          {#each d3.range(0, 100) as number}
            {#if number < n}
              <div class="cuad lleno">
                <img class="buevito" src="./public/images/huevo.png" alt="buevito" style="transform: rotate(180deg);">
              </div>
            {:else}
              <div class="cuad vacio"></div>
            {/if}
          {/each}
        </div>
        
      </div>
    
      {/each}
    </div>
</div>

<p class="titulo-de-graf"> Otras formas de ver los datos</p>
<div class="graficos-f">
  <div class="flourish-embed flourish-chart" data-src="visualisation/19448565"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/19448565/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
  <div class="flourish-embed flourish-chart" data-src="visualisation/19448458"><script src="https://public.flourish.studio/resources/embed.js"></script><noscript><img src="https://public.flourish.studio/visualisation/19448458/thumbnail" width="100%" alt="chart visualization" /></noscript></div>
</div>

<div class="footer">
  <p class="name"> Juan Martin Goyeneche</p>
  <h1>cfkrf</h1>


</div>

<style>
   .cant {
    text-align: center;
    color:#c0975a;
    margin-bottom: 0%;
  }

  .waffles_container {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    gap: 10px;
    background-color: #498a49;

  }

  .waffle {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: repeat(10, 1fr);
    grid-auto-flow: column-reverse;
    transform: rotateX(180deg);
    width: 100%;
    height: 100%;
    gap: 1px;
    background-color: #eee;
    margin-bottom: 10%;
  }
  .cuad {
    font-size: 5px;
    width: 10px;
    height: 13px;
  }
  .vacio {
    background-color: #ddd;
  }
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