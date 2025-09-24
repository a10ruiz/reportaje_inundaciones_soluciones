<script>
  import Scrolly from "../helpers/Scrolly.svelte";
  import { charts, dataTexts } from "../data/chartData.js";

  export let value = 0;
</script>

<section>
  <div class="sticky">
    <div class="chart-container">
      <iframe title="Gráfico" src={charts[0]} scrolling="no" frameborder="0"
      ></iframe>
    </div>
  </div>

  <div class="steps">
    <Scrolly bind:value>
      {#each dataTexts as text, i}
        <div class="step" class:active={value === i}>
          <div class="step-content">
            <p>{@html text}</p>
          </div>
        </div>
      {/each}
    </Scrolly>
  </div>
</section>

<style>
  /* Para saber en que step estamos */


  section {
    position: relative;
  }

  .sticky {
    position: sticky;
    top: 10vh;
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }

  .chart-container {
    position: relative;
    width: 100%;
    height: 100%;
  }

  .chart-container iframe {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100%;
    height: 100%;
    transform: translate(-50%, -50%);
    border: none;
    z-index: 0;
    width: 100%;
    height: 100%;
    border: none;
  }

  .steps {
    position: relative;
    pointer-events: none;
    z-index: 2;
  }

  .step {
    height: 90vh; /* Altura del x% de la ventana gráfica */
    opacity: 0.3; /* Opacidad inicial baja */
    transition: opacity 300ms ease; /* Transición suave de opacidad */
    display: flex; /* Usamos flexbox para centrar el contenido */
    justify-content: center; 
    margin-bottom: 60vh;
  }

  .step.active {
    opacity: 1;
  }

  .step-content {
    padding: 0.9rem 1.2rem;
    border: 1px solid black;
    border-radius: 3px;
    background: white;
    width: 70%;
    height: 30%;
  }

  @media (max-width: 768px) {

    .step {
        width: 100vw;
        z-index: -1;
        margin-bottom: 0px;
        padding-left: 0px;
    }
    .steps {
        position: relative;
        width: 100vw;
        align-items: center;
        justify-content: center;
    }

    .step-content {
        height: 50%;
        width: 80vw;
    }
}

</style>
