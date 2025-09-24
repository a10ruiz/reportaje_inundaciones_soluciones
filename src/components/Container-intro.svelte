<script>
    import Scrolly from "../helpers/Scrolly.svelte";
    import { images as imageDana, texts as textDana } from "../data/scrolldana.js";
    import { onMount } from "svelte";

    let currentValue = 0;
    let showIntro = true;

const handleScroll = () => {
    const scrollTop = window.scrollY;
    showIntro = scrollTop <= window.innerHeight * 0.2;
};

const adjustIntroMargin = () => {
    const header = document.querySelector("header"); // Asegúrate de que el header tiene esta etiqueta o cambia el selector
    const introContainer = document.querySelector(".intro-container");

    if (header && introContainer) {
        const headerHeight = header.offsetHeight;
        introContainer.style.marginTop = `${headerHeight}px`;
    }
};

onMount(() => {
    window.addEventListener("scroll", handleScroll);
    window.addEventListener("resize", adjustIntroMargin);

    adjustIntroMargin(); // Llamar cuando se monta el componente

    return () => {
        window.removeEventListener("scroll", handleScroll);
        window.removeEventListener("resize", adjustIntroMargin);
    };
});
</script>

<section id="DanaScrollSection">
    <!-- Contenedor de inicio con la primera imagen de Scrolly -->
    <div class="intro-container" class:hidden={!showIntro}>
        <div class="intro-overlay">
            <h1 id="titular">
                Antes, durante y después: el complejo puzle que hay que completar para protegerse de las inundaciones 
              </h1>
              <p id="subtitulo">
                Cada vez hay más inundaciones. Para reducir su impacto no hay soluciones mágicas: hacen falta una comunicación clara, construir infraestructuras eficientes adaptadas a cada sitio y abordar de forma completa la legilsación y las zonas en riesgo
              </p>
              <div class="spacer_titu"></div>

              <!-- Espacio en blanco entre los bloques -->
              <div class="spacer_titu"></div>


              <p id="autor">
                <br>
                <svg height="9" width="50%" class="linea-scroll">
                    <line
                      x1="0"
                      y1="0"
                      x2="100%"
                      y2="0"
                      style="stroke:white;stroke-width:5;"
                    />
                  </svg><br>
                Desliza para comenzar ↓ 
            </p>
        </div>
    </div>

    <!-- Contenedor principal del efecto scrolly -->
    <div class="DanaScrollSticky">
        <div class="DanaScrollContainer">
            {#each imageDana as image, i}
                <img src={image} alt="Imagen" class:active={currentValue === i} />
            {/each}
        </div>
    </div>

    <!-- Sección de pasos con el efecto scrolly -->
    <div class="DanaScrollSteps">
        <Scrolly bind:value={currentValue}>
            {#each textDana as text, i}
                <div class="DanaScrollStep" class:active={currentValue === i}>
                    <div class="DanaScrollContent">
                        <p>{@html text.content}</p>
                    </div>
                </div>
            {/each}
        </Scrolly>
    </div>
</section>

<style>

        /* Texto inicio */
        .intro-overlay {
        color: white;
        margin: 0 25%;
        padding: 1%;
        border-radius: 10px;
        justify-content: center;
    }

    .spacer_titu {
        margin: 3% 0;
    }

#titular {
    font-size: 3rem;
    text-align: center; /* Alinea el texto a la izquierda */
    padding: 0.9rem;
    font-weight: 650;
    line-height: 1.1;
  }

  #subtitulo {
    font-size: 1.3rem;
    font-weight: 500;
    font-style: italic;
    text-align: center; /* Alinea el texto a la izquierda */
    margin-top: 3%;
  }


  #logo_autor_scroll {
      width: 35%;
      margin-top: 0 auto;
  }

  .linea-scroll {
    margin: 0 auto;
  }


    /* Contenedor de inicio */
    .intro-container {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        z-index: 10;
        overflow: hidden;
        transition: opacity 0.8s ease, transform 0.8s ease;
        background: linear-gradient(180deg,#000 0,rgba(0,0,0,.5) 110%,transparent)
    }

    .intro-container.hidden {
        opacity: 0;
        transform: translateY(-100%);
        pointer-events: none;
    }

    .DanaScrollContainer img:first-child {
    opacity: 1 !important;
}


    /* Scroll principal */
    .DanaScrollSticky {
        position: sticky;
        top: 0;
        display: flex;
        align-content: center;
    }

    .DanaScrollContainer {
        position: relative;
        display: flex;
        width: 100vw;
        height: 100vh;
        justify-content: center;
        overflow: hidden;
    }

    .DanaScrollContainer img {
        position: absolute;
        object-fit: contain;
        opacity: 0;
        max-width: 100%;
        max-height: 100%;
        transition: opacity 0.5s linear;
    }

    .DanaScrollContainer img.active {
        opacity: 1;
    }

    .DanaScrollSteps {
        position: relative;
        z-index: 2;
    }

    .DanaScrollStep {
        height: 90vh;
        opacity: 0.3;
        transition: opacity 300ms ease;
        display: flex;
        justify-content: left;
        place-items: center;
        padding-left: 17.7%;
    }

    .DanaScrollStep.active {
        opacity: 1;
    }

    .DanaScrollContent {
        padding: 0.9rem 1.2rem;
        border-radius: 3px;
        background: white;
        width: 30%;
        margin-bottom: 60vh;
    }

      /* Mobile adaptations */
  @media (max-width: 768px) {

    .intro-overlay {
        margin: 0 5%;
        padding: 3%;
        top: 10%;
    }

    #titular {
        font-size: 1.8rem;
        padding: 0.6rem;
    }

    #subtitulo {
        font-size: 1rem;
    }

    #logo_autor_scroll {
        width: 60%;
        max-width: 120px;
    }

.DanaScrollContainer {
    height: 45vh;  
    background-color: white; 
}


.DanaScrollContainer img {  
    transform:scale(1.8) translate(-20%, 0%);    
}

.DanaScrollSteps {
    z-index: -1;
}

.DanaScrollStep {
    justify-content: center;
    place-items: center;
    padding-left: 0;
}

.DanaScrollContent {
    width: 100%;
    margin-bottom: 0;
}

}
</style>
