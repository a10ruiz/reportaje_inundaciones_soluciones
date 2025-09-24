<script>
    import Scrolly from "../helpers/Scrolly.svelte";
    import {
        images as imageScrollImages,
        texts as imageScrollTexts,
    } from "../data/imageData.js";

    export let currentValue = 0;

</script>

<section id="imageScrollSection">
    <div class="imageScrollSticky">
        <div class="imageScrollContainer">
{#each imageScrollImages as image, i}
    <img
        src={image}
        alt="Imagen"
        class:active={currentValue === i}
        class:fixed={currentValue >= imageScrollImages.length - 1 && i === imageScrollImages.length - 1}
    />
{/each}

        </div>
    </div>

    <div class="imageScrollSteps">
        <Scrolly bind:value={currentValue}>
            {#each imageScrollTexts as text, i}
                <div class="imageScrollStep" class:active={currentValue === i}>
                    <div class="imageScrollContent" class:active={currentValue === i}>
                        <h1>{text.marjaltitle}</h1>
                        <p>{text.marjal1}{@html text.marjal2}{text.marjal3}"</p>
                    </div>
                </div>
            {/each}
        </Scrolly>
    </div>
</section>

<style>
    @keyframes imageScrollFadeIn {
        from {
            opacity: 0.5;
        }
        to {
            opacity: 1;
        }
    }

    #imageScrollSection {
        position: relative;
    }

    .imageScrollSticky {
        position: sticky;
        top: 0;
    }

    .imageScrollContainer {
        position: relative;
        display: flex;
        width: 100vw;
        height: 100vh;
        align-items: center;
        overflow: hidden;
    }

    .imageScrollContainer img {
        position: absolute;
        object-fit: contain;
        opacity: 0;
        max-width: 80%;
        max-height: 80%;
        z-index: 0;
        transition: opacity 1s ease-in-out;
        margin-top: 65.3px;
    }

    .imageScrollContainer img.active {
        opacity: 1;
        animation: imageScrollFadeIn 1s ease-in-out forwards;
        z-index: 1;
    }

    .imageScrollContainer img.fixed {
        opacity: 1 !important;
    animation: none !important; /* Evita animaciones que podrían hacer que desaparezca */
    transition: none !important;
    }

    .imageScrollSteps {
        position: relative;
        z-index: 2;
    }

    .imageScrollStep {
        height: 105vh;
        opacity: 1;
        transition: opacity 300ms linear;
        display: flex;
        justify-content: right;
    }

/*     .imageScrollStep.active {
        opacity: 1;
    } */

    .imageScrollContent.active {
        background-color: rgb(255, 255, 255);
        border: 2px grey;
        border-style: double;
        transition: background-color 200ms ease-in-out;
    }

    .imageScrollContent {
        padding: 0.9rem 1.2rem;
        border-radius: 10px;
        background: rgb(255, 255, 255);
        width: 35%;
        height: fit-content;
        margin: 7%;
        transition: all 200ms linear;
    }

    .imageScrollContent h1 {
        margin: 0;
        font-weight: 700;
        margin-bottom: 0.6rem;
        font-size: 1.2rem;
    }
    .imageScrollContent p {
        margin: 0;
        font-size: 0.9rem;
        line-height: normal;
    }

    @media (max-width: 768px) {

.imageScrollContainer {
    height: 50vh;  
    background-color: white;    
}


.imageScrollContainer img {
    max-width: 100%;
    max-height: 100%;       
}

.imageScrollSteps {
    z-index: -1;
}

.imageScrollStep {
    justify-content: center;
    place-items: center;
    padding-left: 0;
    width: 100%;
}

.imageScrollContent {
    width: 100%;
    margin-bottom: 0;
    padding: 15%;
}

}
</style>
