<script>
    export let data;
    export let xScale;
    export let yScale;
    export let width;

    $: console.log(tooltipWidth + x > width);

    let tooltipWidth;
    // usamos las escalas que ya hemos creado y usado para los círculos: así el tooltip aparecerá en la misma posición (es un poco como replicar lo de los circulos pero para que aparezca en X ocasiones y no un círculo sino un tooltip)
    $: x = xScale(data.order);
    $: y = yScale(data.startYear);

    $: xPosition = innerWidth < 768 ? x + xNudge : tooltipWidth + x > width ? x - tooltipWidth - xNudge : x + xNudge;
    $: yPosition = y + yNudge;

    const xNudge = -60;
    const yNudge = 30;

    import { fade } from "svelte/transition";
</script>

<!-- Creamos un div para que englobe el tooltip y aparezca en el punto donde ponemos el ratón y no al final de la página-->
<div
    transition:fade
    bind:clientWidth={tooltipWidth}
    class="tooltip"
    style="left: {xPosition}px; top: {yPosition}px;"
>
    <!-- Aquí irá el contenido del tooltip (se incluye como un HTML normal)-->
    <h1 class="tooltip-title">{data.name}</h1> 
    <p class="tooltip-text">ocurrió el <span class="tooltip-date">{data.startDate} </span>
    y ocasionó <span  class="tooltip-date">{data.totalDeaths} muertes</span></p>
</div>

<style>
    .tooltip {
        position: absolute;
        padding: 8px 6px;
        background: white;
        box-shadow: rgba(0, 0, 0, 0.15) 2px 3px 8px;
        border-radius: 3px;
        pointer-events: none; /* Esto es para que no se puedan hacer clic en el tooltip, solo en los círculos*/
        transition:
            top 300ms ease,
            left 300ms ease;

        text-align: center;
        line-height: 1.3;
    }

    .tooltip-title {
        font-size: 0.9rem;
        font-weight: 700;
        text-transform: uppercase;
        margin-bottom: 6px;
        width: 100%;
    }

    .tooltip-text {
        font-size: 0.8rem;
        font-weight: 500;
    }

    .tooltip-date {
        font-size: 0.8rem;
        font-family: 500;
        padding: 2px 4px;
        background-color: #078484a8;
        margin-left: 2px;
        display: inline-block;
        border-radius: 3px;
    }

    @media (max-width: 768px) {
        .tooltip-title{
            font-size: 0.8rem;
        }

        .tooltip-text{
            font-size: 0.7rem;
        }

        .tooltip-date{
            font-size: 0.7rem;
        }
    }

</style>
