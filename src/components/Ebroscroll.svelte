<script>
    import Scrolly from "../helpers/Scrolly.svelte";
    import {
        images as EbroScrollImages,
        texts as EbroScrollTexts,
    } from "../data/EbroData.js";

    export let currentValue = 0;

</script>

<section id="EbroScrollSection">
    <div class="EbroScrollSticky">
        <div class="EbroScrollContainer">
{#each EbroScrollImages as image, i}
    <img
        src={image}
        alt="Imagen"
        class:active={currentValue === i}
        class:fixed={currentValue >= EbroScrollImages.length - 1 && i === EbroScrollImages.length - 1}
    />
{/each}

        </div>
    </div>

    <div class="EbroScrollSteps">
        <Scrolly bind:value={currentValue}>
            {#each EbroScrollTexts as text, i}
                <div class="EbroScrollStep" class:active={currentValue === i}>
                    <div class="EbroScrollContent" class:active={currentValue === i}>
                        <p>{text.ebrotexto}</p>
                    </div>
                </div>
            {/each}
        </Scrolly>
    </div>
</section>

<style>
    @keyframes EbroScrollFadeIn {
        from {
            opacity: 0.5;
        }
        to {
            opacity: 1;
        }
    }

    #EbroScrollSection {
        position: relative;
    }

    .EbroScrollSticky {
        position: sticky;
        top: 0;
    }

    .EbroScrollContainer {
        position: relative;
        display: flex;
        width: 60vw;
        height: 100vh;
        align-items: center;
        overflow: hidden;
    }

    .EbroScrollContainer img {
        position: absolute;
        object-fit: contain;
        opacity: 0;
        max-width: 80%;
        max-height: 80%;
        z-index: 0;
        transition: opacity 1s ease-in-out;
        margin-top: 65.3px;
    }

    .EbroScrollContainer img.active {
        opacity: 1;
        animation: EbroScrollFadeIn 1s ease-in-out forwards;
        z-index: 1;
    }

    .EbroScrollContainer img.fixed {
        opacity: 1 !important;
    animation: none !important; /* Evita animaciones que podrían hacer que desaparezca */
    transition: none !important;
    }

    .EbroScrollSteps {
        position: relative;
        z-index: 2;
    }

    .EbroScrollStep {
        height: 105vh;
        opacity: 1;
        transition: opacity 300ms linear;
        display: flex;
        justify-content: right;
    }

/*     .EbroScrollStep.active {
        opacity: 1;
    } */

    .EbroScrollContent.active {
        background-color: rgb(255, 255, 255);
        border: 2px grey;
        border-style: double;
        transition: background-color 200ms ease-in-out;
    }

    .EbroScrollContent {
        padding: 0.9rem 1.2rem;
        border-radius: 10px;
        background: rgb(255, 255, 255);
        width: 35%;
        height: fit-content;
        margin: 7%;
        transition: all 200ms linear;
    }

    .EbroScrollContent p {
        margin: 0;
        font-size: 0.9rem;
        line-height: normal;
    }

    @media (max-width: 768px) {

.EbroScrollContainer {
    height: 50vh;  
    background-color: white;    
}


.EbroScrollContainer img {
    max-width: 100%;
    max-height: 100%;       
}

.EbroScrollSteps {
    z-index: -1;
}

.EbroScrollStep {
    justify-content: center;
    place-items: center;
    padding-left: 0;
    width: 100%;
}

.EbroScrollContent {
    width: 100%;
    margin-bottom: 0;
    padding: 15%;
}

}
</style>
