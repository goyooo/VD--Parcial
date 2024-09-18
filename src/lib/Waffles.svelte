<script>
    import * as d3 from "d3"
  const years = [2014 , 2015 , 2016 , 2017 , 2018 , 2019 , 2020 , 2021 , 2022 , 2023 ]
  export let numbers = []
</script>

<div class="waffles_container">

  {#each numbers as n}

  <div class="waffle_wrapper">
    <p class="cant">{n}</p>
    <div class="waffle">
      
      {#each d3.range(0, 100) as number}
        {#if number < n}
          <div class="cuad lleno">
            <img class="buevito" src="./src/images/huevo.png" alt="buevito" style="transform: rotate(180deg);">
          </div>
        {:else}
          <div class="cuad vacio"></div>
        {/if}
      {/each}
    </div>
    
  </div>

  {/each}
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

</style>
