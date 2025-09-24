<script>
    export let yScale;
    export let width;
    $: yTicks = yScale.ticks(3); // utilizamos la funcion ticks de scale que te da ticks de forma automatica (no siempre exactamente el numero que pones, pero lo intenta en base a los datos que tienens)
</script>

<g>

      <!-- Título del eje Y -->
  <text 
  x="30"   
  y="-35"  
  text-anchor="middle"
  font-size="15" 
  fill="#000" 
  font-weight="bold">
  Año ⬇️
</text>

    {#each yTicks as tick, index}
        <g class="tick" transform="translate(0, {yScale(tick)})">
            <line
                x1="0"
                y1="0"
                y2="0"
                x2={width}
                stroke={index === 0 ? "#8f8f8f" : "#e5e7eb"}
            ></line>
            <text x="0" y="-4"> {tick}
                {index == yTicks.length - 1? "" : ""}</text>
        </g>
    {/each}
</g>
