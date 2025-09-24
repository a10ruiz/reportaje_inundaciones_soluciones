<script>
    import Scrolly from "../helpers/Scrolly.svelte";
    import { data, scatterText } from "$data/data1.js";
    import { scaleLinear } from "d3-scale";
    import AxisY from "$components/AxisY.svelte";
    import Tooltip from "$components/Tooltip.svelte";
    import { fly } from "svelte/transition";

    const margin = {
        top: 100,
        right: 20,
        bottom: 100,
        left: 0,
    };

    let width = 0; // Inicializamos la anchura
    let height = 0; // Inicializamos la altura
    let innerWidth = 0;
    let innerHeight = 0;

    // Relación de aspecto (2:1) altura mayor que ancho
    const aspectRatioHeightToWidth = 2.6; // 2 veces más alto que ancho

    // Escalas
    $: xScale = scaleLinear().domain([0, 0]).range([0, innerWidth]);

    $: yScale = scaleLinear()
        .domain([
            Math.max(...filteredData.map((d) => d.startYear)),
            Math.min(...filteredData.map((d) => d.startYear)),
        ])
        .range([innerHeight, 0]);

    let rScale = scaleLinear()
        .domain([0, 600])
        .range([
            window.innerWidth > 768 ? 6 : 2.6,
            window.innerWidth > 768 ? 25 : 15,
        ]); // El radio de los círculos varía entre 5 píxeles y 25 píxeles para pantallas anchas (>768px) y 15 píxeles en pantallas estrechas. Esto es para que los círculos se vean bien en diferentes tamaños de pantalla.

    let hoveredData;
    export let value = 0;

    // Datos filtrados según el valor de "value"
    $: filteredData = data.filter((d) => {
        if (value === 1) {
            return d.startYear < 1970;
        } else if (value === 2) {
            return d.startYear >= 1970 && d.startYear < 2000;
        } else if (value === 3) {
            return d.startYear >= 2000;
        }
        return true;
    });

    $: {
        if (value === 0) {
            hoveredData = null;
        } else if (value === 1) {
            hoveredData = filteredData[3];
        } else if (value === 2) {
            hoveredData = filteredData[9];
        } else if (value === 3) {
            hoveredData = filteredData[0];
        }
    }

    // Recalculamos el tamaño del gráfico al montar
    $: {
        // Ajustamos el ancho del gráfico a 60% del viewport
        width = window.innerWidth * 0.6; // Ancho = 60% del viewport

        // Calculamos la altura en base al ancho, manteniendo la relación 2:1 (altura mayor que ancho)
        height = width * aspectRatioHeightToWidth;

        // Aseguramos que la altura no exceda la altura máxima disponible en la ventana
        height = Math.min(height, window.innerHeight);

        // Recalculamos las dimensiones internas del gráfico
        innerWidth = width - margin.left - margin.right;
        innerHeight = height - margin.top - margin.bottom;
    }
</script>

<section id="parte0">
    <div class="SCsticky">
        <div
            class="SCchart-container"
            bind:clientWidth={width}
            bind:clientHeight={height}
            on:mouseleave={() => {
                hoveredData = null;
            }}
            on:touchend={() => {
                hoveredData = null;
            }}
        >
            <svg id="chart" {width} {height}>
                <g transform="translate({margin.left}, {margin.top})">
                    <AxisY {yScale} width={innerWidth} />
                    {#each filteredData as d}
                        <!-- svelte-ignore a11y-mouse-events-have-key-events -->
                        <circle
                            in:fly={{
                                x: -10,
                                opacity: 0,
                                duration: 1000,
                            }}
                            cx={xScale(d.order)}
                            cy={yScale(d.startYear)}
                            r={rScale(d.totalDeaths)}
                            opacity={hoveredData
                                ? hoveredData === d
                                    ? 1
                                    : 0.5
                                : 1}
                            fill="#078484a8"
                            stroke="black"
                            stroke-width="1"
                            on:mouseover={() => {
                                hoveredData = d;
                            }}
                            on:touchstart={() => {
                                hoveredData = d;
                            }}
                        />
                    {/each}
                </g>
            </svg>
            {#if hoveredData}
                <Tooltip
                    data={hoveredData}
                    {xScale}
                    {yScale}
                    width={innerWidth}
                />
            {/if}
        </div>
    </div>

    <div class="SCsteps-container">
        <Scrolly bind:value>
            {#each scatterText as ScatterText, i}
                <div class="SCstep" class:active={value === i}>
                    <div class="SCstep-content">
                        <div>{@html ScatterText}</div>
                    </div>
                </div>
            {/each}
        </Scrolly>
    </div>
</section>

<style>
    :global(.tick text, .axis-label) {
        font-weight: 400;
        font-size: 12px;
        fill: #000000;
        opacity: 80%;
    }

    .SCstep-content :global(b),
    .SCstep-content :global(strong) {
        font-weight: bold !important;
    }

    circle {
        transition:
            r 300ms ease,
            opacity 500ms ease;
    }

    #parte0 {
        text-align: center;
        transition: background 100ms;
        display: flex;
    }

    .SCsticky {
        position: sticky;
        top: 3%;
        display: flex;
        width: 60vw; /* El contenedor se ajusta al 60% del viewport */
        height: 100vh; /* Ocupa toda la altura de la ventana */
        min-height: 100vh;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }

    .SCchart-container {
        width: 100%;
        height: 100%;
        display: flex;
        align-items: stretch;
        overflow-y: hidden;
    }

    .SCstep {
        height: 90vh;
        display: flex;
        place-items: center;
        justify-content: center;
    }

    .SCstep-content {
        font-size: 1rem;
        background: whitesmoke;
        color: #ccc;
        border-radius: 5px;
        padding: 0.5rem 1rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        transition: background 500ms ease;
        box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.2);
        text-align: left;
        width: 75%;
        margin: auto;
        max-width: 500px;
        line-height: normal;
    }

    .SCstep.active .SCstep-content {
        background: white;
        color: black;
    }

    .SCsteps-container,
    .SCsticky {
        height: 100%;
    }

    .SCsteps-container {
        flex: 1 1 40%;
        z-index: 10;
    }

    @media (max-width: 480px) {
        #parte0 {
            position: relative;
            display: unset;
        }

        .SCsticky {
            margin: 0 auto;
        }

        .SCsteps-container {
            position: relative;
            flex: none;
            z-index: 3;
        }

        .SCstep {
            height: 110vh;
            margin-bottom: 60%;
        }

        .SCchart-container {
            display: unset;
            height: fit-content;
        }

        .SCstep-content {
            font-size: 0.9rem;
        }
    }
</style>
