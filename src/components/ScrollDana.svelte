<script>
    import Scrolly from "../helpers/Scrolly.svelte";
    import {
        images as imageDana,
        texts as textDana,
    } from "../data/scrolldana.js";

    export let currentValue = 0;


</script>

<section id="DanaScrollSection">
    <div class="DanaScrollSticky">
        <div class="DanaScrollContainer">
{#each imageDana as image, i}
    <img
        src={image}
        alt="Imagen"
        class:active={currentValue === i}
    />
{/each}

        </div>
    </div>

    <div class="DanaScrollSteps">
        <Scrolly bind:value={currentValue}>
            {#each textDana as text, i}
                <div class="DanaScrollStep"  class:stayVisible={currentValue >= imageDana.length - 1 && i === imageDana.length - 1} class:active={currentValue === i}
                >
                    <div class="DanaScrollContent">
                        <p>{text.content}</p>
                    </div>
                </div>
            {/each}
        </Scrolly>
    </div>
</section>

<style>

@keyframes DanaScrollFadeIn {
        from {
            opacity: 0.5;
        }
        to {
            opacity: 1;
        }
    }


    #DanaScrollSection {
        position: relative;
    }

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
        z-index: 0;
        margin-top: 65.3px;
        transition: opacity 0.5s linear;
    }

    .DanaScrollContainer img.active {
        opacity: 1;
        animation: DanaScrollFadeIn 0.5s linear;
        z-index: 1;
    }

    .DanaScrollContainer img.stayVisible {
    opacity: 1 !important;
    animation: none !important; /* Evita animaciones que podrían hacer que desaparezca */
    transition: none !important;
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
        /* margin-bottom: 10vh; */
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

    .DanaScrollContent p {
        margin: 0;
        font-size: 0.9rem;
        line-height: normal;
    }

  /* Mobile adaptations */
  @media (max-width: 768px) {

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
