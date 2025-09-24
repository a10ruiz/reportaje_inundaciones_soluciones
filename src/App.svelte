<script>
  import PuzzleMenu from "./components/PuzzleMenu.svelte";
  import Scatter from "./components/Scatter.svelte";
  import ImageScroll from "./components/Parquealicante.svelte";
  import Galeriamarjal from "./components/Galleriamarjal.svelte";
  import Galeriagavardaybenexida from "./components/Galeriagavarda.svelte";
  import Contenedorintro from "./components/Container-intro.svelte";
  import Ebroscroll from "./components/Ebroscroll.svelte";

  let value = 0; // Variable que almacena el valor actual del scrolly
</script>

<main>
  <div class="contenido">
    <Contenedorintro bind:value />

    <!--TEXTO PRUEBA -->
    <span style="margin-top: 4rem;"></span>
    <p>
      La DANA de octubre de 2024 afectó a 78 municipios, principalmente en la
      provincia de Valencia pero también en Albacete y Málaga, dejando 224
      personas fallecidas, tres desaparecidas y numerosos daños materiales en
      poblaciones y zonas agrarias. El coste ya <a
        href="https://www.lamoncloa.gob.es/info-dana/Paginas/2025/180225-datos-seguimiento-actuaciones-gobierno.aspx"
        ><u>supera los 3.000 millones</u></a
      >
      de euros. El desastre también trajo consigo una campaña de ruido y
      <a
        href="https://maldita.es/clima/20241121/desinformaciones-DANA-causas-agua/"
        ><u>desinformación</u></a
      > y muchas preguntas: ¿qué se hizo mal? ¿Se pueden evitar catástrofes así?
    </p>

    <p>
      Las inundaciones siempre han existido, pero su frecuencia <a
        href="https://www.nature.com/articles/s41586-020-2478-3"
        ><u>está aumentando</u></a
      > en las últimas décadas.
    </p>

    <!--SECCIÓN SCATTER INTRO -->
    <section class="grafico">
      <Scatter bind:value />
    </section>

    <!-- PÁRRAFO POST SCATTER -->
    <p>
      Cada inundación es diferente. La comunidad científica lleva décadas
      desarrollando soluciones adaptadas a cada tipo de inundación en cada lugar
      y en cada fase del fenómeno. No hay una solución única. Como en un puzle,
      unas necesitan de las otras.
    </p>

    <p>
      Sigue deslizando para verlas todas o pulsa en la que más te interese:
    </p>

    <div class="spacer"></div>

    <!-- PUZZLE MENU -->
    <PuzzleMenu bind:value />

    <!-- SECCIÓN PARTE 1 -->

    <section id="parte1">
      <div style="height: 26vh;"></div>
      <h2>
        Sistema de alerta temprana ante inundaciones rápidas: del modelo japonés
        al español
      </h2>

      <div class="contenedorimgtextoscroll">
        <img
          class="imgtxtscroll"
          src="https://files.maldita.es/maldita/uploads/2025/02/67c1ce2d5568cfile-jpg.jpg"
          alt="TsunamiJapón"
        />
        <p class="piefotoscroll">
          Tsunami que arrasó la costa noreste de Japón, en 2011 (JIJI PRESS
          /AFP)
        </p>
      </div>
      <p>
        El 11 de marzo de 2011, un <b>terremoto de magnitud 9</b> sacudió una
        zona cercana a la<b> costa este de Japón</b> provocando un tsunami que
        envolvió​ ​su litoral en lo que fue la mayor catástrofe en el país desde
        la II Guerra Mundial. Murieron casi
        <a
          href="https://www.reconstruction.go.jp/english/topics/GEJE/index.html"
          ><u>20.000 personas</u></a
        >, otras 2.500 siguen oficialmente desaparecidas y más de un millón de
        edificios resultaron afectados o destruidos, incluyendo carreteras, vías
        de tren y aeropuertos.
      </p>

      <p>
        La inmensa inundación <a
          href="https://www.nrc.gov/reading-rm/doc-collections/fact-sheets/japan-events.html"
          ><u>desencadenó</u></a
        >
        además el accidente en la <b>central nuclear de Fukushima</b>, pues al
        impactar sobre los reactores destruyó el suministro energético que
        permitía refrigerarlos. El aumento de temperatura en varios de ellos
        derivó en una explosión que liberó toneladas de material radioactivo.
        Aún hoy continúan los trabajos de descontaminación.
      </p>

      <p>
        Más de 470.000 personas fueron evacuadas. En febrero del año pasado, aún
        quedaban 29.000 personas fuera de sus hogares, el 90% de ellas de la
        prefectura de Fukushima, según los <a
          href="https://www.reconstruction.go.jp/english/topics/Progress_to_date/English_August_2024_genjoutorikumi-E.pdf#page=16"
          ><u>informes</u></a
        >
        que todavía elabora la Agencia de Reconstrucción japonesa. La triple catástrofe
        afectó a las prefecturas de Fukushima, Iwate y Miyagi, donde se encuentra<b
        >
        </b>la <b>ciudad costera de Sendai</b>.
      </p>

      <p>
        Y <b> </b>ese fue precisamente el nombre que recibió el
        <a
          href="https://www.undrr.org/publication/sendai-framework-disaster-risk-reduction-2015-2030"
          ><u>Marco de Sendai para la reducción del riesgo de desastres</u></a
        >, firmado tres años más tarde por los países de Naciones Unidas para
        reducir las muertes en todo tipo de catástrofes mediante
        <b> sistemas de alerta temprana</b> (SAT). Estos programas combinan la tecnología
        para predecir riesgos naturales en tiempo real con la coordinación entre
        las autoridades y la información de la ciudadanía para salvar vidas.
      </p>

      <p>
        Desde febrero de 2007 Japón ya contaba con <a
          href="https://centreforpublicimpact.org/public-impact-fundamentals/j-alert-disaster-warning-technology-in-japan/#The-initiative"
          ><u>su sistema</u></a
        >
        de alerta temprana, <b>llamado J-Alert</b>, que funcionaba previendo
        riesgos vía satélite y transmitiendo alertas claras a las instituciones
        locales y la ciudadanía a través de altavoces. Tras la tragedia de 2011
        se subsanaron algunas deficiencias y ahora “podría considerarse que
        <b> Japón tiene uno de los mejores</b>” en el mundo, explica a
        <i>Maldita.es</i>
        <a href="https://www.reading.ac.uk/ges/staff/jeff-da-costa"
          ><u>Jeff Da Costa</u></a
        >, investigador en la Universidad de Reading, en Reino Unido.
      </p>

      <p>
        “Su éxito radica en la<b> fuerte coordinación </b>entre la agencia
        meteorológica japonesa y las instituciones locales”, detalla Da Costa.
        También se debe a “la experiencia que tiene Japón en grandes desastres y
        la <b>disciplina de su población</b>”, añade
        <a href="https://x.com/maloycia"><u>Guillermo Malo</u></a>, exsuboficial
        mayor de la Unidad Militar de Emergencias. De hecho, un día antes de la
        DANA, la embajada japonesa en España
        <a
          href="https://maldita.es/malditobulo/20241106/sms-embajada-japon-espana-dana/"
          ><u>envió dos correos electrónicos</u></a
        > a los ciudadanos de su país residentes en el nuestro para informar sobre
        la previsión de lluvias y recordar que tomaran medidas de autoprotección.
      </p>


      <p>
        El cambio climático está <a
          href="https://ntrs.nasa.gov/citations/20230009525"
          ><u>aumentando la frecuencia</u></a
        >
        de las
        <a
          href="https://unterm.un.org/unterm2/en/view/66f7422a-6ec9-449c-ab48-72d811f08896#:~:text=Crecida%20que%20sube%20repentinamente%2C%20con%20poco%20o%20ning%C3%BAn%20aviso%20previo.%20Suele%20ser%20el%20resultado%20de%20lluvias%20intensas%20ca%C3%ADdas%20sobre%20una%20zona%20reducida.%20Hay%20otras%20causas%20posibles%2C%20como%20atascos%20por%20hielo%2C%20roturas%20de%20presas%2C%20etc."
          ><u>inundaciones repentinas</u></a
        >
        a nivel global. Se trata de inundaciones donde el intervalo de tiempo entre
        el fenómeno que las causa (normalmente, lluvias torrenciales) y la aparición
        de la inundación es de
        <a
          href="https://www.sciencedirect.com/science/article/abs/pii/S2212420924007866"
          ><u>6 horas o menos</u></a
        >. Son las más agresivas de todas las inundaciones y se estima que cada
        año provocan unas
        <a href="https://wmo.int/projects/ffgs"><u>5.000 muertes</u></a> en todo
        el mundo.
      </p>

      <p>
        En el caso de Valencia, la <a
          href="https://maldita.es/clima/20241108/cronologia-avisos-rio-magro-rambla-poyo/"
          ><u>cronología</u></a
        >
        estuvo marcada por dos momentos clave: en torno a las
        <a
          href="https://maldita.es/clima/20241108/cronologia-avisos-rio-magro-rambla-poyo/"
          ><u>07:30 horas</u></a
        >
        del 29 de octubre, la Agencia Estatal de Meteorología
        <b> elevó a rojos los avisos por lluvias </b>en el norte de la provincia
        de Valencia, pero no fue hasta las
        <a
          href="https://maldita.es/clima/20241108/cronologia-avisos-rio-magro-rambla-poyo/"
          ><u>20:11 horas</u></a
        >
        cuando la Generalitat Valenciana emitió la
        <b>alerta móvil ES-Alert</b>. Para entonces el temporal ya había dejado
        barrancos desbordados y crecidas en distintos ríos. Algunos
        ayuntamientos alertaron a sus ciudadanos cuando la inundación
        <a href="https://x.com/Ajunt_Paiporta/status/1851320374270832897"
          ><u>ya estaba sucediendo</u></a
        >.
      </p>

      <div class="contenedorimgtextoscroll" style="width=50%;">
        <img
          class="imgtxtscrollalerta"
          src="https://files.maldita.es/maldita/uploads/2025/02/67c1e69a5ff86photo-2025-02-28-17-37-43-jpg.jpg"
          alt="alertaDanaValencia"
        />
        <p class="piefotoscroll">
          Alerta móvil de la DANA de Valencia a las 20:12
        </p>
      </div>

      <p>
        ¿Tiene España un sistema de alerta temprana frente a inundaciones? “La
        herramienta <a
          href="https://www.proteccioncivil.es/coordinacion/redes/ran/public-warning-system"
          ><u>ES-Alert</u></a
        >
        es importante, pero su eficacia depende de la calidad de la información<b
        >
        </b>en la que se basa. La AEMET emite avisos meteorológicas y las
        confederaciones hidrográficas controlan el nivel de los ríos y el riesgo
        de inundaciones. Aunque esos programas son importantes,
        <b> no son un SAT completo en sentido técnico</b>”, responde Da Costa,
        que está especializado en SAT contra emergencias hidrológicas.
      </p>

      <p>
        La definición de SAT tiene cuatro componentes clave: conocimiento del
        riesgo, seguimiento y previsión, difusión de alertas y capacidad de
        respuesta. “Aunque España incorpora aspectos de estos componentes, sigue
        habiendo problemas a la hora de traducir las previsiones en alertas, <b
          >garantizar una comunicación clara</b
        >
        entre las distintas regiones y <b>mejorar la preparación de las comunidades</b>”, explica.
      </p>

      <p>
        Coincide Guillermo Malo: “Es muy necesario que se unifiquen sistemas y
        criterios técnicos, teniendo en cuenta que al estar <a
          href="https://www.boe.es/buscar/act.php?id=BOE-A-2015-7730#a14"
          ><u>transferidas las competencias</u></a
        >
        en protección civil tenemos <b>17 sistemas diferentes</b>, que muchas
        veces no se entienden entre ellos”. Salvo para el riesgo nuclear y
        bélico, que son competencia estatal, las comunidades autónomas
        <a href="https://www.boe.es/buscar/act.php?id=BOE-A-2015-7730#a14"
          ><u>deben elaborar</u></a
        > planes territoriales de emergencia sobre todo tipo de riesgos.
      </p>

      <p>
        Además, los municipios con más de 20.000 habitantes <a
          href="https://www.boe.es/buscar/act.php?id=BOE-A-1985-5392#a26"
          ><u>deben disponer del servicio</u></a
        >
        de protección civil, aunque en abril del año pasado 61 municipios valencianos
        obligados a tener un
        <b>plan municipal de emergencias</b> todavía<b> </b>no lo habían
        aprobado, según
        <a
          href="https://www.112cv.gva.es/documents/163565706/174325491/NVL_PlanMun.pdf/ca7c9b7f-9c81-453d-9b4e-141851174a31?t=1657275473212"
          ><u>un balance de la Generalitat</u></a
        >, y de los 227 que debían contar con un
        <b>plan frente a inundaciones</b>, sólo el 70% lo tenían en vigor.
        <b>Paiporta</b>, por ejemplo, no había constancia de ninguno de los dos.
      </p>

      <p>
        Los sistemas de alerta temprana avanzados salvan vidas antes de que una
        inundación se produzca. Por su parte, las infraestructuras en ríos y
        ciudades, que alivian el impacto del agua y reducen daños materiales
        cuando el suceso ya está ocurriendo. Son la siguiente pieza del puzle.
      </p>

      <svg
        class="icono-texto"
        viewBox="0 0 300 450"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        zoomAndPan="magnify"
        preserveAspectRatio="xMidYMid meet"
        version="1.0"
        ><defs
          ><clipPath id="06e8dfb3f4"
            ><path
              d="M 34 43 L 299 43 L 299 309 L 34 309 Z M 34 43 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="9a74a42c8e"
            ><path
              d="M 175.960938 43.6875 L 337.4375 229.269531 L 195.421875 352.839844 L 33.945312 167.261719 Z M 175.960938 43.6875 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="bb558b1e3c"
            ><path
              d="M 175.960938 43.6875 L 337.4375 229.269531 L 195.421875 352.839844 L 33.945312 167.261719 Z M 175.960938 43.6875 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="874e7dfaed"
            ><path
              d="M 175.960938 43.6875 L 337.4375 229.269531 L 195.421875 352.839844 L 33.945312 167.261719 Z M 175.960938 43.6875 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="8cbfa28aaa"
            ><path
              d="M 82 21.886719 L 266.339844 21.886719 L 266.339844 274 L 82 274 Z M 82 21.886719 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="143baaae17"
            ><path
              d="M 65.339844 268 L 110 268 L 110 316.636719 L 65.339844 316.636719 Z M 65.339844 268 "
              clip-rule="nonzero"
            /></clipPath
          ></defs
        ><g clip-path="url(#06e8dfb3f4)"
          ><g clip-path="url(#9a74a42c8e)"
            ><g clip-path="url(#bb558b1e3c)"
              ><g clip-path="url(#874e7dfaed)"
                ><path
                  fill="#000000"
                  d="M 276.703125 254.089844 C 268.636719 244.824219 255.726562 254.660156 249.132812 247.082031 C 242.539062 239.503906 251.664062 226.433594 251.664062 226.433594 L 298.878906 185.351562 L 257.722656 138.050781 C 257.722656 138.050781 244.640625 128.90625 237.074219 135.492188 C 229.503906 142.078125 239.355469 155.003906 230.101562 163.058594 C 220.847656 171.113281 202.769531 163.476562 193.402344 152.714844 C 184.015625 141.925781 178.976562 122.992188 188.230469 114.9375 C 197.484375 106.882812 208.925781 118.429688 216.496094 111.84375 C 224.0625 105.257812 216.816406 91.039062 216.816406 91.039062 L 175.699219 43.789062 L 34.320312 166.808594 L 157.496094 308.371094 L 204.710938 267.289062 C 204.710938 267.289062 218.917969 260.058594 225.511719 267.632812 C 232.105469 275.210938 220.578125 286.640625 228.640625 295.910156 C 236.707031 305.175781 255.65625 300.136719 266.40625 290.78125 C 277.152344 281.429688 284.765625 263.359375 276.703125 254.089844 Z M 276.703125 254.089844 "
                  fill-opacity="1"
                  fill-rule="nonzero"
                /></g
              ></g
            ></g
          ></g
        ><g clip-path="url(#8cbfa28aaa)"
          ><path
            fill="#ca4b34"
            d="M 84.609375 273.433594 C 84.472656 273.433594 84.332031 273.433594 84.238281 273.386719 C 83.300781 273.152344 82.691406 272.21875 82.925781 271.28125 C 84.003906 266.699219 85.453125 262.113281 87.230469 257.667969 C 87.605469 256.78125 88.632812 256.359375 89.523438 256.6875 C 90.410156 257.0625 90.832031 258.089844 90.503906 258.980469 C 88.773438 263.28125 87.371094 267.679688 86.34375 272.078125 C 86.109375 272.917969 85.40625 273.433594 84.609375 273.433594 Z M 95.042969 247.519531 C 94.714844 247.519531 94.433594 247.425781 94.15625 247.285156 C 93.3125 246.769531 93.03125 245.742188 93.546875 244.898438 C 95.980469 240.828125 98.691406 236.851562 101.6875 233.15625 C 102.292969 232.410156 103.417969 232.269531 104.164062 232.875 C 104.914062 233.484375 105.054688 234.605469 104.445312 235.355469 C 101.59375 238.910156 98.925781 242.746094 96.632812 246.675781 C 96.210938 247.191406 95.605469 247.519531 95.042969 247.519531 Z M 112.585938 225.71875 C 112.117188 225.71875 111.648438 225.53125 111.277344 225.15625 C 110.621094 224.457031 110.667969 223.332031 111.371094 222.679688 C 114.878906 219.449219 118.667969 216.457031 122.550781 213.789062 C 123.34375 213.230469 124.421875 213.460938 124.980469 214.257812 C 125.542969 215.054688 125.308594 216.175781 124.515625 216.691406 C 120.773438 219.214844 117.125 222.117188 113.753906 225.25 C 113.425781 225.578125 113.007812 225.71875 112.585938 225.71875 Z M 135.742188 210.046875 C 135.085938 210.046875 134.476562 209.671875 134.152344 209.066406 C 133.730469 208.175781 134.105469 207.148438 134.992188 206.726562 C 135.789062 206.351562 136.582031 205.976562 137.425781 205.652344 C 140.605469 204.246094 144.160156 202.9375 148.277344 201.582031 C 149.167969 201.300781 150.195312 201.769531 150.476562 202.703125 C 150.757812 203.640625 150.289062 204.621094 149.355469 204.902344 C 145.332031 206.210938 141.917969 207.523438 138.78125 208.878906 C 137.988281 209.207031 137.238281 209.578125 136.488281 209.90625 C 136.210938 210 135.976562 210.046875 135.742188 210.046875 Z M 162.21875 200.878906 C 161.46875 200.878906 160.769531 200.363281 160.535156 199.617188 C 160.253906 198.679688 160.769531 197.699219 161.703125 197.464844 C 166.476562 196.0625 170.777344 194.796875 175.035156 193.300781 C 175.925781 192.972656 176.953125 193.488281 177.28125 194.375 C 177.609375 195.3125 177.09375 196.292969 176.207031 196.621094 C 171.902344 198.117188 167.550781 199.382812 162.734375 200.832031 C 162.546875 200.878906 162.40625 200.878906 162.21875 200.878906 Z M 188.601562 191.382812 C 187.949219 191.382812 187.339844 191.007812 187.011719 190.398438 C 186.589844 189.558594 186.917969 188.484375 187.808594 188.0625 C 192.203125 185.863281 195.898438 183.429688 199.175781 180.625 C 199.921875 180.015625 201 180.0625 201.652344 180.8125 C 202.261719 181.558594 202.214844 182.636719 201.464844 183.289062 C 198.003906 186.238281 194.074219 188.808594 189.398438 191.195312 C 189.117188 191.335938 188.835938 191.382812 188.601562 191.382812 Z M 209.464844 173.183594 C 209.136719 173.183594 208.8125 173.09375 208.53125 172.90625 C 207.734375 172.390625 207.453125 171.3125 207.96875 170.472656 C 210.261719 166.871094 212.179688 162.847656 213.769531 158.167969 C 214.097656 157.234375 215.125 156.765625 216.015625 157.09375 C 216.949219 157.421875 217.417969 158.402344 217.089844 159.339844 C 215.40625 164.25 213.394531 168.507812 210.917969 172.390625 C 210.636719 172.90625 210.027344 173.183594 209.464844 173.183594 Z M 219.007812 146.941406 C 218.914062 146.941406 218.773438 146.941406 218.679688 146.894531 C 217.746094 146.707031 217.089844 145.773438 217.277344 144.835938 C 217.886719 141.609375 218.496094 138.054688 219.054688 133.703125 L 219.382812 131.082031 C 219.523438 130.101562 220.367188 129.445312 221.347656 129.585938 C 222.332031 129.726562 222.984375 130.570312 222.84375 131.550781 L 222.515625 134.21875 C 221.910156 138.664062 221.347656 142.21875 220.691406 145.539062 C 220.554688 146.378906 219.804688 146.941406 219.007812 146.941406 Z M 171.667969 129.164062 C 171.667969 129.164062 171.621094 129.164062 171.621094 129.164062 L 170.917969 129.164062 C 169.9375 129.164062 169.1875 128.324219 169.1875 127.386719 C 169.1875 126.40625 170.078125 125.65625 170.964844 125.65625 L 171.574219 125.65625 C 171.574219 125.65625 171.621094 125.65625 171.621094 125.65625 C 175.738281 125.65625 180.089844 125.238281 184.53125 124.347656 C 185.515625 124.160156 186.402344 124.769531 186.589844 125.75 C 186.777344 126.6875 186.167969 127.621094 185.1875 127.808594 C 180.554688 128.699219 176.019531 129.164062 171.667969 129.164062 Z M 157.121094 127.199219 C 156.980469 127.199219 156.792969 127.199219 156.605469 127.15625 C 155.808594 126.921875 155.015625 126.6875 154.21875 126.40625 C 150.429688 125.097656 146.828125 123.226562 143.507812 120.839844 C 142.710938 120.277344 142.523438 119.203125 143.085938 118.40625 C 143.648438 117.609375 144.769531 117.425781 145.519531 117.984375 C 148.605469 120.183594 151.878906 121.914062 155.34375 123.085938 C 156.089844 123.320312 156.792969 123.550781 157.539062 123.785156 C 158.476562 124.066406 158.992188 125.050781 158.710938 125.984375 C 158.570312 126.6875 157.867188 127.199219 157.121094 127.199219 Z M 198.378906 123.972656 C 197.675781 123.972656 196.976562 123.550781 196.742188 122.851562 C 196.414062 121.960938 196.882812 120.933594 197.769531 120.605469 C 202.027344 119.015625 206.238281 117.097656 210.261719 114.851562 C 211.101562 114.382812 212.179688 114.664062 212.648438 115.554688 C 213.113281 116.394531 212.789062 117.472656 211.945312 117.9375 C 207.734375 120.277344 203.382812 122.242188 198.988281 123.925781 C 198.800781 123.925781 198.566406 123.972656 198.378906 123.972656 Z M 222.5625 119.109375 C 222.515625 119.109375 222.472656 119.109375 222.425781 119.109375 C 221.441406 119.0625 220.738281 118.21875 220.785156 117.238281 C 220.972656 114.476562 221.113281 111.8125 221.160156 109.285156 C 221.019531 108.910156 221.019531 108.441406 221.160156 108.066406 C 221.160156 107.414062 221.160156 106.757812 221.160156 106.058594 C 221.160156 105.167969 221.160156 104.230469 221.113281 103.34375 C 221.113281 102.359375 221.863281 101.566406 222.84375 101.566406 C 222.84375 101.566406 222.890625 101.566406 222.890625 101.566406 C 223.828125 101.566406 224.621094 102.3125 224.667969 103.296875 C 224.667969 103.859375 224.667969 104.417969 224.667969 104.980469 C 227.242188 102.875 229.769531 100.628906 232.152344 98.246094 C 232.855469 97.542969 233.933594 97.589844 234.632812 98.246094 C 235.335938 98.945312 235.335938 100.023438 234.632812 100.722656 C 231.5 103.859375 228.132812 106.804688 224.667969 109.472656 C 224.621094 112.042969 224.480469 114.664062 224.296875 117.472656 C 224.25 118.40625 223.5 119.109375 222.5625 119.109375 Z M 134.570312 111.34375 C 134.058594 111.34375 133.496094 111.109375 133.167969 110.640625 C 130.269531 106.804688 127.929688 102.5 126.199219 97.964844 C 125.871094 97.074219 126.292969 96.046875 127.226562 95.71875 C 128.117188 95.390625 129.144531 95.8125 129.472656 96.746094 C 131.109375 101.003906 133.261719 104.980469 135.976562 108.582031 C 136.535156 109.378906 136.394531 110.453125 135.601562 111.015625 C 135.273438 111.203125 134.898438 111.34375 134.570312 111.34375 Z M 221.816406 91.132812 C 220.972656 91.132812 220.226562 90.527344 220.085938 89.636719 C 219.664062 86.832031 219.101562 84.070312 218.449219 81.449219 C 218.027344 79.71875 217.511719 77.988281 216.949219 76.304688 C 216.625 75.371094 217.136719 74.386719 218.074219 74.105469 C 219.007812 73.777344 219.992188 74.292969 220.273438 75.230469 C 220.878906 77.007812 221.394531 78.832031 221.863281 80.65625 C 222.5625 83.414062 223.125 86.269531 223.59375 89.214844 C 223.734375 90.152344 223.078125 91.085938 222.097656 91.226562 C 222.003906 91.132812 221.910156 91.132812 221.816406 91.132812 Z M 242.726562 90.761719 C 242.351562 90.761719 241.976562 90.621094 241.652344 90.386719 C 240.902344 89.777344 240.714844 88.703125 241.324219 87.90625 C 244.128906 84.257812 246.703125 80.421875 248.996094 76.445312 C 249.460938 75.601562 250.539062 75.324219 251.378906 75.789062 C 252.222656 76.257812 252.503906 77.335938 252.035156 78.175781 C 249.648438 82.246094 246.984375 86.222656 244.082031 90.011719 C 243.753906 90.527344 243.242188 90.761719 242.726562 90.761719 Z M 124.75 85.425781 C 123.859375 85.425781 123.0625 84.726562 123.015625 83.789062 C 122.921875 82.574219 122.878906 81.402344 122.878906 80.1875 C 122.878906 76.445312 123.34375 72.796875 124.234375 69.289062 C 124.46875 68.351562 125.449219 67.792969 126.386719 68.023438 C 127.320312 68.257812 127.882812 69.195312 127.648438 70.175781 C 126.851562 73.40625 126.433594 76.773438 126.433594 80.1875 C 126.433594 81.308594 126.480469 82.433594 126.574219 83.507812 C 126.667969 84.492188 125.917969 85.332031 124.933594 85.378906 C 124.796875 85.425781 124.75 85.425781 124.75 85.425781 Z M 256.808594 66.527344 C 256.574219 66.527344 256.339844 66.480469 256.152344 66.386719 C 255.261719 66.011719 254.84375 64.984375 255.214844 64.09375 C 256.992188 59.839844 258.492188 55.441406 259.613281 51.042969 C 259.847656 50.109375 260.785156 49.546875 261.765625 49.78125 C 262.703125 50.015625 263.261719 50.996094 263.027344 51.933594 C 261.8125 56.46875 260.316406 61.007812 258.445312 65.453125 C 258.117188 66.152344 257.460938 66.527344 256.808594 66.527344 Z M 212.925781 64.65625 C 212.320312 64.65625 211.710938 64.328125 211.382812 63.769531 C 209.046875 59.699219 206.378906 56.003906 203.382812 52.773438 C 202.730469 52.074219 202.777344 50.949219 203.476562 50.296875 C 204.179688 49.640625 205.300781 49.6875 205.957031 50.390625 C 209.136719 53.804688 211.992188 57.734375 214.472656 62.039062 C 214.9375 62.878906 214.660156 63.957031 213.816406 64.421875 C 213.535156 64.609375 213.207031 64.65625 212.925781 64.65625 Z M 131.625 58.761719 C 131.296875 58.761719 130.921875 58.667969 130.640625 58.433594 C 129.847656 57.875 129.613281 56.796875 130.175781 56.003906 C 132.839844 52.074219 136.210938 48.519531 140.140625 45.476562 C 140.886719 44.867188 142.011719 45.007812 142.617188 45.804688 C 143.226562 46.554688 143.085938 47.675781 142.289062 48.285156 C 138.640625 51.136719 135.554688 54.410156 133.074219 58.015625 C 132.746094 58.527344 132.1875 58.761719 131.625 58.761719 Z M 193.886719 44.449219 C 193.5625 44.449219 193.28125 44.355469 192.953125 44.214844 C 191.410156 43.277344 189.773438 42.390625 188.132812 41.6875 C 185.75 40.613281 183.175781 39.769531 180.554688 39.160156 C 179.621094 38.976562 179.011719 37.992188 179.199219 37.058594 C 179.433594 36.121094 180.324219 35.511719 181.304688 35.699219 C 184.160156 36.355469 186.964844 37.242188 189.585938 38.414062 C 191.363281 39.207031 193.09375 40.144531 194.777344 41.171875 C 195.621094 41.6875 195.851562 42.765625 195.386719 43.605469 C 195.058594 44.167969 194.449219 44.449219 193.886719 44.449219 Z M 153.378906 41.6875 C 152.675781 41.6875 152.019531 41.265625 151.738281 40.566406 C 151.367188 39.675781 151.832031 38.648438 152.722656 38.273438 C 157.308594 36.449219 162.03125 35.324219 166.804688 34.859375 C 167.832031 34.765625 168.628906 35.464844 168.722656 36.449219 C 168.816406 37.429688 168.113281 38.273438 167.128906 38.367188 C 162.6875 38.789062 158.289062 39.863281 154.03125 41.546875 C 153.796875 41.6875 153.609375 41.6875 153.378906 41.6875 Z M 263.871094 39.488281 C 263.824219 39.488281 263.730469 39.488281 263.683594 39.488281 C 262.703125 39.394531 262.046875 38.507812 262.140625 37.523438 C 262.515625 34.109375 262.746094 30.648438 262.746094 27.234375 C 262.746094 26.0625 262.746094 24.894531 262.703125 23.769531 C 262.65625 22.789062 263.402344 21.992188 264.386719 21.945312 C 265.367188 22.039062 266.164062 22.648438 266.210938 23.632812 C 266.257812 24.847656 266.257812 26.015625 266.257812 27.234375 C 266.257812 30.789062 266.070312 34.390625 265.648438 37.898438 C 265.507812 38.835938 264.757812 39.488281 263.871094 39.488281 Z M 263.871094 39.488281 "
            fill-opacity="1"
            fill-rule="nonzero"
          /></g
        ><g clip-path="url(#143baaae17)"
          ><path
            fill="#ca4b34"
            d="M 109.683594 276.289062 L 76.425781 316.378906 L 65.199219 268.710938 L 83.253906 282.183594 Z M 109.683594 276.289062 "
            fill-opacity="1"
            fill-rule="nonzero"
          /></g
        ></svg
      >
    </section>

    <!-- SECCIÓN PARTE 2 -->

    <section id="parte2">
      <div style="height: 1vh;"></div>

      <h2>
        El parque La Marjal en Alicante y el proyecto Ebro Resilience: cuando la
        planificación funciona
      </h2>
      <div class="contenedorimgtextoscroll">
        <img
          class="imgtxtscroll"
          src="https://files.maldita.es/maldita/uploads/2025/02/67c1cf078bd26file-jpg.jpg"
          alt="TsunamiJapón"
        />
        <p class="piefotoscroll">
          Varias chicas descansan en el Parque La Marjal de Alicante
        </p>
      </div>

      <p>
        Con las personas a resguardo, las infraestructuras construidas en ríos o
        ciudades actúan mientras la inundación se está produciendo. Las que
        vamos a describir <b>no son aplicables a la DANA de Valencia</b> porque están
        diseñadas para lugares y tipos de inundación distintos, como recuerdan los
        expertos consultados.
      </p>

      <p>
        Las inundaciones que afectan a las ciudades pueden ser <b>pluviales</b>,
        cuando cae lluvia intensa sobre la ciudad, y <b>fluviales</b>, cuando un
        río sale de su cauce y vierte su caudal sobre las calles a toda
        velocidad, explica
        <a href="http://www.upv.es/ficha-personal/igando"
          ><u>Ignacio Andrés Doménech</u></a
        >, ingeniero en el departamento de Ingeniería Hidráulica y Medio
        Ambiente en la Universitat Politècnica de València. En <b>Alicante</b>,
        junto a la famosa playa de San Juan, existe un proyecto que actúa cuando
        se da el primer caso: el <b>Parque de inundación La Marjal</b>.
      </p>

      <p>
        La ciudad de Alicante creció ocupando zonas donde antes solían
        producirse inundaciones de forma natural, llamadas marjales. Pese a la
        construcción de una red que canalizaba el agua de la lluvia hacia el
        mar, ciertas áreas seguían inundándose en episodios de lluvias intensas,
        explica la
        <a
          href="https://adaptecca.es/casos-practicos/parque-de-inundacion-la-marjal"
          ><u>Adaptatecca</u></a
        >, una plataforma sobre la adaptación al cambio climático en España.
      </p>

      <p>
        En 2011, desde el ayuntamiento se ideó una forma de almacenar el
        excedente que no podía asumir la red de evacuación. Situado precisamente
        en un antiguo marjal, el parque funciona como un gran depósito. Su
        capacidad total es de 45.000 m3, “suficiente para almacenar
        temporalmente el agua excedente de una lluvia de 50 años de <a
          href="https://www.fnca.eu/guia-nueva-cultura-del-agua/glosario/57-"
          ><u>período de retorno</u></a
        >”, es decir, de tal intensidad que solo se produce una vez cada 50
        años, aproximadamente.
      </p>

      <ImageScroll bind:value />

      <p>
        Pero además, durante el año el parque sirve como espacio de recreo para
        los alicantinos y es un hogar para la flora y la fauna autóctonas al
        tiempo que permite reutilizar el agua acumulada en el riego de otros
        parques y jardines.
      </p>

      <p>
        Construir La Marjal tuvo un coste total de 3,3 millones de euros, que
        financió al completo la empresa municipal Aguas Municipalizadas de
        Alicante. Las obras comenzaron en 2013 y finalizaron el 27 de marzo de
        2015, creando una nueva zona verde urbana que este año cumple su primera
        década. Desde entonces, el parque ya ha frenado varias posibles
        inundaciones en la zona.
      </p>

      <p>
        En marzo de 2017, cuando se produjo el tercer evento de lluvias más
        copiosas en la ciudad desde 1934, La Marjal recogió parte de esa lluvia
        alcanzando el <b>34% de su capacidad</b>. En 2019, una madrugada de
        agosto registró la mayor precipitación acumulada en la ciudad en 150
        años y<b> el parque se llenó hasta el 50%</b>, según la
        <a
          href="https://adaptecca.es/casos-practicos/parque-de-inundacion-la-marjal"
          ><u>Adaptatecca</u></a
        >.
      </p>

      <Galeriamarjal />

      <p>
        El parque La Marjal es sólo uno de los múltiples <b>Sistemas Urbanos</b>
        <b>de Drenaje Sostenible</b> o SUDS que se están instalando en muchas ciudades
        españolas en los últimos años. Su ventaja es que son soluciones “perfectamente
        replicables” para aliviar el impacto de inundaciones de tipo pluvial y “asumibles”
        por las instituciones locales, que son quienes los gestionan e instalan,
        explica Doménech.
      </p>

      <p>
        Su principal limitación es “la necesidad de espacio para implantarlas,
        algo no siempre obvio en ciudades o territorios altamente ocupados”, y
        para compensarlo a veces se opta por<b> sistemas híbridos </b>que
        combinan estas soluciones basadas en la naturaleza con soluciones más
        convencionales, como el alcantarillado. Puedes explorar los SUDS
        españoles en el siguiente mapa.<br /><br />

        <iframe
          title="SUDS en España"
          aria-label="Mapa"
          id="datawrapper-chart-GVjEr"
          src="https://datawrapper.dwcdn.net/GVjEr/3/"
          scrolling="no"
          frameborder="0"
          style="width: 0; min-width: 100% !important; border: none;"
          height="650"
          data-external="1"
        ></iframe><script type="text/javascript">
          !(function () {
            "use strict";
            window.addEventListener("message", function (a) {
              if (void 0 !== a.data["datawrapper-height"]) {
                var e = document.querySelectorAll("iframe");
                for (var t in a.data["datawrapper-height"])
                  for (var r = 0; r < e.length; r++)
                    if (e[r].contentWindow === a.source) {
                      var i = a.data["datawrapper-height"][t] + "px";
                      e[r].style.height = i;
                    }
              }
            });
          })();
        </script>
      </p>

      <h3>
        <i>Ebro Resilience</i> o cuando la colaboración administrativa funciona
      </h3>

      <p>
        El tramo medio del río Ebro abarca desde la ciudad de Logroño hasta La
        Zaida, en la provincia de Zaragoza, formando un <b
          >inmenso valle con muy poca pendiente</b
        >
        donde florece la agricultura. En este tramo del río,
        <a href="https://www.ebroresilience.com/ebro-resilience/antecedentes/"
          ><font color="#1155cc"
            ><u>las inundaciones son muy frecuentes</u></font
          ></a
        >: hay una crecida ordinaria todos los años y, cada cierto tiempo, una
        extraordinaria que suele perjudicar los cultivos aledaños. No es una
        sorpresa, pues
        <b
          >están situados precisamente en la llanura que ha creado el propio río</b
        > con sus inundaciones recurrentes.
      </p>

      <p>
        En 2015 tuvieron lugar tres crecidas extraordinarias en los primeros
        cuatro meses del año, provocando daños que tuvieron un coste superior a <a
          href="https://www.ebroresilience.com/proyecto-life-p1/el-proyecto/#:~:text=entre%20actuaciones%20de%20emergencia%20para%20la%20reparaci%C3%B3n%20del%20encauzamiento%20de%20la%20Confederaci%C3%B3n%20Hidrogr%C3%A1fica%20del%20Ebro%20y%20ayudas%20de%20las%20Comunidades%20Aut%C3%B3nomas%20se%20invirtieron%2054%2C6%20millones%20de%20euros%20en%20La%20Rioja%2C%20Navarra%20y%20Arag%C3%B3n."
          ><font color="#1155cc"><u>50 millones de euros</u></font></a
        >. Para evitar que se repitiera esa situación, en agosto de 2015 el, en
        aquel entonces, Ministerio de Agricultura y Pesca, Alimentación y Medio
        Ambiente convocó una reunión para crear un programa de defensa ante
        inundaciones en el que colaborasen todas las administraciones
        relacionadas con ese tramo medio del Ebro, sembrando la semilla de
        <b>Ebro Resilience</b>, cuenta a <i>Maldita.es</i> el ingeniero
        <a href="https://www.youtube.com/watch?v=-D2QqF-vGNI"
          ><font color="#1155cc"><u>David Gargantilla</u></font></a
        >, el actual director técnico del proyecto.<br />
        <br />
        La idea es conseguir “un cambio en la gestión de las inundaciones” con “una
        combinación de medidas novedosas en <b>18 tramos del Ebro medio</b>”,
        <a href="https://www.ebroresilience.com/proyecto-life-p1/el-proyecto/"
          ><font color="#1155cc"><u>explica la web</u></font></a
        >. En cada zona se estudia el comportamiento del río teniendo en cuenta
        las experiencias pasadas y se aplican medidas específicas según las
        necesidades. Por un lado los embalses regulan el caudal máximo del río y
        se refuerzan algunos diques para evitar desbordamientos, pero también
        <a
          href="https://www.youtube.com/watch?v=JwK_MNoNwO4&amp;feature=youtu.be"
          ><font color="#1155cc"><u>se eliminan otros</u></font></a
        >
        o se crean
        <a
          href="https://www.ebroresilience.com/cauce-de-alivio-meandro-la-roza-corredor-ribereno/"
          ><font color="#1155cc"><u>cauces de alivio</u></font></a
        >, es decir, se abren nuevos brazos al río para reducir el caudal que
        pasa por cada uno.
      </p>

      <p>
        Una de las medidas que mejor ha funcionado y que ahora están replicando
        en nuevas zonas del río, son las<b> áreas de inundación temporal</b>,
        cuyo objetivo es reducir los daños en los cultivos anexos al río cuando
        ocurran las inevitables crecidas. “Cuando el río se desborda, va a
        ocupar su llanura de inundación. Eso es natural y no puede evitarse. Lo
        que puedes hacer es, en esa llanura de inundación, reducir los daños<b>
          ¿Cómo? Inundándola antes</b
        >”, explica Gargantilla.
      </p>

      <p>
        Cuando se prevé una crecida, que en el tramo medio del Ebro puede
        estimarse con holgada antelación, gracias a la nivelación de los
        terrenos se preinunda una zona concreta con muy poca altura. “Esa agua <b
          >funciona como un colchón</b
        >” que evita que, cuando el río se desborda o rompe el dique de
        protección, haga socavones o arrample con caminos, acequias o sistemas
        de riego.
      </p>

      <Ebroscroll bind:value />

      <!--SCROLL EBRO FALTA !!!!!!!!!!!!!!!!!!!!!!!! -->

      <p>
        En la aplicación de esas medidas participan, en uno u otro grado, la
        Dirección General del Agua del MITECO, la Confederación Hidrográfica del
        Ebro, los Gobiernos autonómicos de Aragón, La Rioja y Navarra y las
        empresas públicas Tragsa y Tragsatec, además de los alcaldes de los
        municipios donde se ejecuta cada medida. “Todas <b
          >las soluciones que se toman se analizan y deciden entre todos</b
        >. Va más allá de la coordinación, es un trabajo conjunto”, añade
        Gargantilla.
      </p>

      <p>
        Ebro Resilience es también un ejercicio de malabarismo que consigue ir
        alternando las fuentes de ingresos y funciones de cada miembro del
        proyecto con agilidad. “Somos<b> omnívoros financieros</b>”, bromea
        Gargantilla, pues algunas actuaciones se están financiando con los
        fondos Next Generation de la Unión Europea, en otras vienen del MITECO y
        en algunas de mayor calibre el dinero proviene de todos los organismos
        implicados más el apoyo de fondos europeos. En algunas intervenciones,
        un organismo pone los fondos, otro distinto ejecuta las obras y el
        ayuntamiento del municipio donde se localizan cede los terrenos.
      </p>

      <p>
        Las dificultades llegan a veces a la hora de comunicar las
        intervenciones a los agricultores y vecinos. “Como muchas medidas que
        hacemos son antiintuitivas, en muchos casos hay reticencia a aplicarlas
        y lo que se pide es hacer más de lo mismo. Pero <b
          >si hacemos más de lo mismo, tendremos más resultados iguales</b
        > a los anteriores. Así que nos encontramos con ese problema por ser los
        primeros en hacerlo de otra forma”, cuenta Gargantilla.
      </p>

      <p>
        “Rebajamos el lenguaje técnico, lo explicamos en lenguaje llano, se
        hacen todas las reuniones que haga falta, llevamos a la gente de un
        sitio a otro” para que conozcan las intervenciones que se hacen en cada
        lugar, explica. Cuentan también con <b
          >profesionales en procesos de participación</b
        >, pues muchas de sus actuaciones necesitan la colaboración voluntaria
        de los agricultores.
      </p>

      <p>
        Alfredo Zaldívar, alcalde de Remolinos (Zaragoza), cuenta que algunos
        vecinos agricultores rechazaban las áreas de inundación controlada
        situadas en ese término municipal porque significaba perjudicar algunos
        de sus cultivos. Fue <b
          >tarea del alcalde, en una conversación de tú a tú</b
        >, recordarles por ejemplo que muchas de esas fincas están en la llanura
        de inundación natural del Ebro: “Hay muchas tierras que han sido
        usurpadas al río”.
      </p>

      <p>
        Además de los sistemas de alertas y las infraestructuras, hay otras
        soluciones que pueden prevenir los riesgos por inundación de forma
        permanente, aunque también son más complicados de diseñar y conseguir:
        como la legislación y la relocalización de algunas poblaciones <b
          >¿La pieza definitiva del puzle?</b
        >
      </p>

      <svg
        class="icono-texto"
        viewBox="0 0 300 450"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        zoomAndPan="magnify"
        preserveAspectRatio="xMidYMid meet"
        version="1.0"
        ><defs
          ><clipPath id="06e8dfb3f4"
            ><path
              d="M 34 43 L 299 43 L 299 309 L 34 309 Z M 34 43 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="9a74a42c8e"
            ><path
              d="M 175.960938 43.6875 L 337.4375 229.269531 L 195.421875 352.839844 L 33.945312 167.261719 Z M 175.960938 43.6875 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="bb558b1e3c"
            ><path
              d="M 175.960938 43.6875 L 337.4375 229.269531 L 195.421875 352.839844 L 33.945312 167.261719 Z M 175.960938 43.6875 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="874e7dfaed"
            ><path
              d="M 175.960938 43.6875 L 337.4375 229.269531 L 195.421875 352.839844 L 33.945312 167.261719 Z M 175.960938 43.6875 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="8cbfa28aaa"
            ><path
              d="M 82 21.886719 L 266.339844 21.886719 L 266.339844 274 L 82 274 Z M 82 21.886719 "
              clip-rule="nonzero"
            /></clipPath
          ><clipPath id="143baaae17"
            ><path
              d="M 65.339844 268 L 110 268 L 110 316.636719 L 65.339844 316.636719 Z M 65.339844 268 "
              clip-rule="nonzero"
            /></clipPath
          ></defs
        ><g clip-path="url(#06e8dfb3f4)"
          ><g clip-path="url(#9a74a42c8e)"
            ><g clip-path="url(#bb558b1e3c)"
              ><g clip-path="url(#874e7dfaed)"
                ><path
                  fill="#000000"
                  d="M 276.703125 254.089844 C 268.636719 244.824219 255.726562 254.660156 249.132812 247.082031 C 242.539062 239.503906 251.664062 226.433594 251.664062 226.433594 L 298.878906 185.351562 L 257.722656 138.050781 C 257.722656 138.050781 244.640625 128.90625 237.074219 135.492188 C 229.503906 142.078125 239.355469 155.003906 230.101562 163.058594 C 220.847656 171.113281 202.769531 163.476562 193.402344 152.714844 C 184.015625 141.925781 178.976562 122.992188 188.230469 114.9375 C 197.484375 106.882812 208.925781 118.429688 216.496094 111.84375 C 224.0625 105.257812 216.816406 91.039062 216.816406 91.039062 L 175.699219 43.789062 L 34.320312 166.808594 L 157.496094 308.371094 L 204.710938 267.289062 C 204.710938 267.289062 218.917969 260.058594 225.511719 267.632812 C 232.105469 275.210938 220.578125 286.640625 228.640625 295.910156 C 236.707031 305.175781 255.65625 300.136719 266.40625 290.78125 C 277.152344 281.429688 284.765625 263.359375 276.703125 254.089844 Z M 276.703125 254.089844 "
                  fill-opacity="1"
                  fill-rule="nonzero"
                /></g
              ></g
            ></g
          ></g
        ><g clip-path="url(#8cbfa28aaa)"
          ><path
            fill="#ca4b34"
            d="M 84.609375 273.433594 C 84.472656 273.433594 84.332031 273.433594 84.238281 273.386719 C 83.300781 273.152344 82.691406 272.21875 82.925781 271.28125 C 84.003906 266.699219 85.453125 262.113281 87.230469 257.667969 C 87.605469 256.78125 88.632812 256.359375 89.523438 256.6875 C 90.410156 257.0625 90.832031 258.089844 90.503906 258.980469 C 88.773438 263.28125 87.371094 267.679688 86.34375 272.078125 C 86.109375 272.917969 85.40625 273.433594 84.609375 273.433594 Z M 95.042969 247.519531 C 94.714844 247.519531 94.433594 247.425781 94.15625 247.285156 C 93.3125 246.769531 93.03125 245.742188 93.546875 244.898438 C 95.980469 240.828125 98.691406 236.851562 101.6875 233.15625 C 102.292969 232.410156 103.417969 232.269531 104.164062 232.875 C 104.914062 233.484375 105.054688 234.605469 104.445312 235.355469 C 101.59375 238.910156 98.925781 242.746094 96.632812 246.675781 C 96.210938 247.191406 95.605469 247.519531 95.042969 247.519531 Z M 112.585938 225.71875 C 112.117188 225.71875 111.648438 225.53125 111.277344 225.15625 C 110.621094 224.457031 110.667969 223.332031 111.371094 222.679688 C 114.878906 219.449219 118.667969 216.457031 122.550781 213.789062 C 123.34375 213.230469 124.421875 213.460938 124.980469 214.257812 C 125.542969 215.054688 125.308594 216.175781 124.515625 216.691406 C 120.773438 219.214844 117.125 222.117188 113.753906 225.25 C 113.425781 225.578125 113.007812 225.71875 112.585938 225.71875 Z M 135.742188 210.046875 C 135.085938 210.046875 134.476562 209.671875 134.152344 209.066406 C 133.730469 208.175781 134.105469 207.148438 134.992188 206.726562 C 135.789062 206.351562 136.582031 205.976562 137.425781 205.652344 C 140.605469 204.246094 144.160156 202.9375 148.277344 201.582031 C 149.167969 201.300781 150.195312 201.769531 150.476562 202.703125 C 150.757812 203.640625 150.289062 204.621094 149.355469 204.902344 C 145.332031 206.210938 141.917969 207.523438 138.78125 208.878906 C 137.988281 209.207031 137.238281 209.578125 136.488281 209.90625 C 136.210938 210 135.976562 210.046875 135.742188 210.046875 Z M 162.21875 200.878906 C 161.46875 200.878906 160.769531 200.363281 160.535156 199.617188 C 160.253906 198.679688 160.769531 197.699219 161.703125 197.464844 C 166.476562 196.0625 170.777344 194.796875 175.035156 193.300781 C 175.925781 192.972656 176.953125 193.488281 177.28125 194.375 C 177.609375 195.3125 177.09375 196.292969 176.207031 196.621094 C 171.902344 198.117188 167.550781 199.382812 162.734375 200.832031 C 162.546875 200.878906 162.40625 200.878906 162.21875 200.878906 Z M 188.601562 191.382812 C 187.949219 191.382812 187.339844 191.007812 187.011719 190.398438 C 186.589844 189.558594 186.917969 188.484375 187.808594 188.0625 C 192.203125 185.863281 195.898438 183.429688 199.175781 180.625 C 199.921875 180.015625 201 180.0625 201.652344 180.8125 C 202.261719 181.558594 202.214844 182.636719 201.464844 183.289062 C 198.003906 186.238281 194.074219 188.808594 189.398438 191.195312 C 189.117188 191.335938 188.835938 191.382812 188.601562 191.382812 Z M 209.464844 173.183594 C 209.136719 173.183594 208.8125 173.09375 208.53125 172.90625 C 207.734375 172.390625 207.453125 171.3125 207.96875 170.472656 C 210.261719 166.871094 212.179688 162.847656 213.769531 158.167969 C 214.097656 157.234375 215.125 156.765625 216.015625 157.09375 C 216.949219 157.421875 217.417969 158.402344 217.089844 159.339844 C 215.40625 164.25 213.394531 168.507812 210.917969 172.390625 C 210.636719 172.90625 210.027344 173.183594 209.464844 173.183594 Z M 219.007812 146.941406 C 218.914062 146.941406 218.773438 146.941406 218.679688 146.894531 C 217.746094 146.707031 217.089844 145.773438 217.277344 144.835938 C 217.886719 141.609375 218.496094 138.054688 219.054688 133.703125 L 219.382812 131.082031 C 219.523438 130.101562 220.367188 129.445312 221.347656 129.585938 C 222.332031 129.726562 222.984375 130.570312 222.84375 131.550781 L 222.515625 134.21875 C 221.910156 138.664062 221.347656 142.21875 220.691406 145.539062 C 220.554688 146.378906 219.804688 146.941406 219.007812 146.941406 Z M 171.667969 129.164062 C 171.667969 129.164062 171.621094 129.164062 171.621094 129.164062 L 170.917969 129.164062 C 169.9375 129.164062 169.1875 128.324219 169.1875 127.386719 C 169.1875 126.40625 170.078125 125.65625 170.964844 125.65625 L 171.574219 125.65625 C 171.574219 125.65625 171.621094 125.65625 171.621094 125.65625 C 175.738281 125.65625 180.089844 125.238281 184.53125 124.347656 C 185.515625 124.160156 186.402344 124.769531 186.589844 125.75 C 186.777344 126.6875 186.167969 127.621094 185.1875 127.808594 C 180.554688 128.699219 176.019531 129.164062 171.667969 129.164062 Z M 157.121094 127.199219 C 156.980469 127.199219 156.792969 127.199219 156.605469 127.15625 C 155.808594 126.921875 155.015625 126.6875 154.21875 126.40625 C 150.429688 125.097656 146.828125 123.226562 143.507812 120.839844 C 142.710938 120.277344 142.523438 119.203125 143.085938 118.40625 C 143.648438 117.609375 144.769531 117.425781 145.519531 117.984375 C 148.605469 120.183594 151.878906 121.914062 155.34375 123.085938 C 156.089844 123.320312 156.792969 123.550781 157.539062 123.785156 C 158.476562 124.066406 158.992188 125.050781 158.710938 125.984375 C 158.570312 126.6875 157.867188 127.199219 157.121094 127.199219 Z M 198.378906 123.972656 C 197.675781 123.972656 196.976562 123.550781 196.742188 122.851562 C 196.414062 121.960938 196.882812 120.933594 197.769531 120.605469 C 202.027344 119.015625 206.238281 117.097656 210.261719 114.851562 C 211.101562 114.382812 212.179688 114.664062 212.648438 115.554688 C 213.113281 116.394531 212.789062 117.472656 211.945312 117.9375 C 207.734375 120.277344 203.382812 122.242188 198.988281 123.925781 C 198.800781 123.925781 198.566406 123.972656 198.378906 123.972656 Z M 222.5625 119.109375 C 222.515625 119.109375 222.472656 119.109375 222.425781 119.109375 C 221.441406 119.0625 220.738281 118.21875 220.785156 117.238281 C 220.972656 114.476562 221.113281 111.8125 221.160156 109.285156 C 221.019531 108.910156 221.019531 108.441406 221.160156 108.066406 C 221.160156 107.414062 221.160156 106.757812 221.160156 106.058594 C 221.160156 105.167969 221.160156 104.230469 221.113281 103.34375 C 221.113281 102.359375 221.863281 101.566406 222.84375 101.566406 C 222.84375 101.566406 222.890625 101.566406 222.890625 101.566406 C 223.828125 101.566406 224.621094 102.3125 224.667969 103.296875 C 224.667969 103.859375 224.667969 104.417969 224.667969 104.980469 C 227.242188 102.875 229.769531 100.628906 232.152344 98.246094 C 232.855469 97.542969 233.933594 97.589844 234.632812 98.246094 C 235.335938 98.945312 235.335938 100.023438 234.632812 100.722656 C 231.5 103.859375 228.132812 106.804688 224.667969 109.472656 C 224.621094 112.042969 224.480469 114.664062 224.296875 117.472656 C 224.25 118.40625 223.5 119.109375 222.5625 119.109375 Z M 134.570312 111.34375 C 134.058594 111.34375 133.496094 111.109375 133.167969 110.640625 C 130.269531 106.804688 127.929688 102.5 126.199219 97.964844 C 125.871094 97.074219 126.292969 96.046875 127.226562 95.71875 C 128.117188 95.390625 129.144531 95.8125 129.472656 96.746094 C 131.109375 101.003906 133.261719 104.980469 135.976562 108.582031 C 136.535156 109.378906 136.394531 110.453125 135.601562 111.015625 C 135.273438 111.203125 134.898438 111.34375 134.570312 111.34375 Z M 221.816406 91.132812 C 220.972656 91.132812 220.226562 90.527344 220.085938 89.636719 C 219.664062 86.832031 219.101562 84.070312 218.449219 81.449219 C 218.027344 79.71875 217.511719 77.988281 216.949219 76.304688 C 216.625 75.371094 217.136719 74.386719 218.074219 74.105469 C 219.007812 73.777344 219.992188 74.292969 220.273438 75.230469 C 220.878906 77.007812 221.394531 78.832031 221.863281 80.65625 C 222.5625 83.414062 223.125 86.269531 223.59375 89.214844 C 223.734375 90.152344 223.078125 91.085938 222.097656 91.226562 C 222.003906 91.132812 221.910156 91.132812 221.816406 91.132812 Z M 242.726562 90.761719 C 242.351562 90.761719 241.976562 90.621094 241.652344 90.386719 C 240.902344 89.777344 240.714844 88.703125 241.324219 87.90625 C 244.128906 84.257812 246.703125 80.421875 248.996094 76.445312 C 249.460938 75.601562 250.539062 75.324219 251.378906 75.789062 C 252.222656 76.257812 252.503906 77.335938 252.035156 78.175781 C 249.648438 82.246094 246.984375 86.222656 244.082031 90.011719 C 243.753906 90.527344 243.242188 90.761719 242.726562 90.761719 Z M 124.75 85.425781 C 123.859375 85.425781 123.0625 84.726562 123.015625 83.789062 C 122.921875 82.574219 122.878906 81.402344 122.878906 80.1875 C 122.878906 76.445312 123.34375 72.796875 124.234375 69.289062 C 124.46875 68.351562 125.449219 67.792969 126.386719 68.023438 C 127.320312 68.257812 127.882812 69.195312 127.648438 70.175781 C 126.851562 73.40625 126.433594 76.773438 126.433594 80.1875 C 126.433594 81.308594 126.480469 82.433594 126.574219 83.507812 C 126.667969 84.492188 125.917969 85.332031 124.933594 85.378906 C 124.796875 85.425781 124.75 85.425781 124.75 85.425781 Z M 256.808594 66.527344 C 256.574219 66.527344 256.339844 66.480469 256.152344 66.386719 C 255.261719 66.011719 254.84375 64.984375 255.214844 64.09375 C 256.992188 59.839844 258.492188 55.441406 259.613281 51.042969 C 259.847656 50.109375 260.785156 49.546875 261.765625 49.78125 C 262.703125 50.015625 263.261719 50.996094 263.027344 51.933594 C 261.8125 56.46875 260.316406 61.007812 258.445312 65.453125 C 258.117188 66.152344 257.460938 66.527344 256.808594 66.527344 Z M 212.925781 64.65625 C 212.320312 64.65625 211.710938 64.328125 211.382812 63.769531 C 209.046875 59.699219 206.378906 56.003906 203.382812 52.773438 C 202.730469 52.074219 202.777344 50.949219 203.476562 50.296875 C 204.179688 49.640625 205.300781 49.6875 205.957031 50.390625 C 209.136719 53.804688 211.992188 57.734375 214.472656 62.039062 C 214.9375 62.878906 214.660156 63.957031 213.816406 64.421875 C 213.535156 64.609375 213.207031 64.65625 212.925781 64.65625 Z M 131.625 58.761719 C 131.296875 58.761719 130.921875 58.667969 130.640625 58.433594 C 129.847656 57.875 129.613281 56.796875 130.175781 56.003906 C 132.839844 52.074219 136.210938 48.519531 140.140625 45.476562 C 140.886719 44.867188 142.011719 45.007812 142.617188 45.804688 C 143.226562 46.554688 143.085938 47.675781 142.289062 48.285156 C 138.640625 51.136719 135.554688 54.410156 133.074219 58.015625 C 132.746094 58.527344 132.1875 58.761719 131.625 58.761719 Z M 193.886719 44.449219 C 193.5625 44.449219 193.28125 44.355469 192.953125 44.214844 C 191.410156 43.277344 189.773438 42.390625 188.132812 41.6875 C 185.75 40.613281 183.175781 39.769531 180.554688 39.160156 C 179.621094 38.976562 179.011719 37.992188 179.199219 37.058594 C 179.433594 36.121094 180.324219 35.511719 181.304688 35.699219 C 184.160156 36.355469 186.964844 37.242188 189.585938 38.414062 C 191.363281 39.207031 193.09375 40.144531 194.777344 41.171875 C 195.621094 41.6875 195.851562 42.765625 195.386719 43.605469 C 195.058594 44.167969 194.449219 44.449219 193.886719 44.449219 Z M 153.378906 41.6875 C 152.675781 41.6875 152.019531 41.265625 151.738281 40.566406 C 151.367188 39.675781 151.832031 38.648438 152.722656 38.273438 C 157.308594 36.449219 162.03125 35.324219 166.804688 34.859375 C 167.832031 34.765625 168.628906 35.464844 168.722656 36.449219 C 168.816406 37.429688 168.113281 38.273438 167.128906 38.367188 C 162.6875 38.789062 158.289062 39.863281 154.03125 41.546875 C 153.796875 41.6875 153.609375 41.6875 153.378906 41.6875 Z M 263.871094 39.488281 C 263.824219 39.488281 263.730469 39.488281 263.683594 39.488281 C 262.703125 39.394531 262.046875 38.507812 262.140625 37.523438 C 262.515625 34.109375 262.746094 30.648438 262.746094 27.234375 C 262.746094 26.0625 262.746094 24.894531 262.703125 23.769531 C 262.65625 22.789062 263.402344 21.992188 264.386719 21.945312 C 265.367188 22.039062 266.164062 22.648438 266.210938 23.632812 C 266.257812 24.847656 266.257812 26.015625 266.257812 27.234375 C 266.257812 30.789062 266.070312 34.390625 265.648438 37.898438 C 265.507812 38.835938 264.757812 39.488281 263.871094 39.488281 Z M 263.871094 39.488281 "
            fill-opacity="1"
            fill-rule="nonzero"
          /></g
        ><g clip-path="url(#143baaae17)"
          ><path
            fill="#ca4b34"
            d="M 109.683594 276.289062 L 76.425781 316.378906 L 65.199219 268.710938 L 83.253906 282.183594 Z M 109.683594 276.289062 "
            fill-opacity="1"
            fill-rule="nonzero"
          /></g
        ></svg
      >
    </section>

    <!-- SECCIÓN PARTE 3 -->

    <div class="spacer"></div>
    <section id="parte3">
      <div style="height: 1vh;"></div>
      <h2>
        ¿Reconstruir los pueblos inundados o trasladarlos a otro lugar para que
        no vuelvan a inundarse? De la experiencia valenciana en Beneixida al
        huracán Katrina en EEUU
      </h2>

      <p>
        Uno de los problemas que tanto expertos como vecinos coinciden en
        señalar sobre la DANA en Valencia es que muchas viviendas estaban
        situadas en zonas inundables. Impedir que se construyan casas en áreas
        de riesgo, e incluso reubicar algunas poblaciones en zonas más seguras,
        parecen entonces soluciones lógicas. Pero de momento ambas opciones
        presentan muchos obstáculos.
      </p>

      <p>
        ¿Por qué se sigue construyendo en zonas inundables del levante español?
        preguntamos a <a
          href="https://cvnet.cpd.ua.es/curriculum-breve/es/olcina-cantos-jorge/5787"
          ><font color="#1155cc"><u>Jorge Olcina-Cantos</u></font></a
        >, doctor en Geografía y profesor de Ordenación del Territorio en la
        Universidad de Alicante. “Porque los planes urbanísticos de los
        municipios españoles son, la mayoría, anteriores a toda exigencia
        ambiental y a la obligación de elaborar mapas de riesgos naturales que
        estableció la <b>ley del suelo de 2008</b>”.
      </p>

      <p>
        Las normas que limitan o prohíben edificar en zonas inundables no se
        aplican a los suelos ya clasificados como urbanizables por planes
        urbanísticos municipales anteriores. El grueso de las edificaciones con
        este problema son las
        <b>c</b><b>onstruidas entre 1960</b>, cuando comenzó el desarrollo
        económico moderno en España, <b>y</b><b> el año </b><b>2008</b>, explica
        el experto.
      </p>

      <p>
        Olcina cree que una moratoria a la construcción en zonas inundables es
        “una solución necesaria”. “Pero junto a ello, [también lo es] el <b
          >desalojo de zonas inundables con alto riesgo para la vida humana
        </b>que están ocupadas urbanísticamente y que se hayan visto afectadas
        por inundaciones en los últimos cincuenta años”, añade. Francia es el
        país con una normativa más exigente en este sentido, cuenta el experto,
        e incluye supuestos de reubicación.
      </p>

      <h3>Gavarda y Beneixida</h3>
      <div class="contenedorimgtextoscroll">
        <img
          class="imgtxtscroll"
          src="https://files.maldita.es/maldita/uploads/2025/02/67bdbe2f2f253file-jpg.jpg"
          alt="Gavarda y Beneixida"
        />
      </div>

      <p>
        En España hay ejemplos de poblaciones que fueron trasladadas a zonas con
        menor riesgo tras una inundación. Es el caso de <a
          href="https://www.google.es/maps/place/Gavarda,+Valencia/@39.078623,-0.5647941,13.97z/data=!4m15!1m8!3m7!1s0xd61a6e09bf845c9:0xb939d13d34d6f8a!2s46267+Gabarda,+Valencia!3b1!8m2!3d39.0913006!4d-0.5602546!16s%2Fm%2F02qdncc!3m5!1s0xd61a69513b2b463:0x5f02b4dad9028cd6!8m2!3d39.0913007!4d-0.5429181!16s%2Fg%2F11cn5p2l05?hl=es&amp;entry=ttu&amp;g_ep=EgoyMDI1MDIyNS4wIKXMDSoASAFQAw%3D%3D"
          ><font color="#1155cc"><u>Gavarda</u></font></a
        >
        y
        <a
          href="https://www.google.es/maps/place/Beneixida,+Valencia/@39.0838145,-0.5780729,13.2z/data=!4m15!1m8!3m7!1s0xd61a6e09bf845c9:0xb939d13d34d6f8a!2s46267+Gabarda,+Valencia!3b1!8m2!3d39.0913006!4d-0.5602546!16s%2Fm%2F02qdncc!3m5!1s0xd61a139917113c7:0xce6bfb1bf0637eeb!8m2!3d39.0577704!4d-0.5487011!16s%2Fg%2F11cn62ydmw?hl=es&amp;entry=ttu&amp;g_ep=EgoyMDI1MDIyNS4wIKXMDSoASAFQAw%3D%3D"
          ><font color="#1155cc"><u>Beneixida</u></font></a
        >, dos pueblos valencianos situados en riberas contrarias del río Júcar.
      </p>

      <p>
        El 20 de octubre de 1982, tras horas de lluvias intensas, la presa de
        Tous, en Valencia, cedió al peso del agua generando un violento
        desbordamiento del río que anegó las calles de esos municipios, en un
        evento que se recuerda como ‘La pantaná’. El agua <b
          >alcanzó hasta ocho metros de altura
        </b>en el caso de Beneixida, cuenta a<i> Maldita.es </i>su actual
        alcaldesa,
        <a href="https://www.beneixida.es/es/pagina/saludo"
          ><font color="#1155cc"><u>Begoña Lluch</u></font></a
        >, que entonces tenía 11 años.
      </p>

      <p>
        Después de la catástrofe, el ayuntamiento de Beneixida solicitó al
        Consejo de Ministros <b>cambiar de ubicación a toda la localidad</b>,
        una solución que fue aprobada el 22 de febrero de 1983, “de ahí la
        fiesta local que perdura desde entonces”, apostilla Lluch. Gavarda
        también se trasladó, aunque en su caso
        <a
          href="https://www.levante-emv.com/pantanada-tous/2022/10/18/municipio-fracturo-pantanada-77415937.html"
          ><font color="#1155cc"
            ><u>algunos vecinos decidieron quedarse</u></font
          ></a
        > en las casas que habían resistido y ahora el pueblo viejo sigue en pie
        formando un mosaico de casas y solares vacíos.
      </p>

      <p>
        En Benexida, la regidora cuenta que
        <b>desde entonces no han sufrido ninguna inundación</b>. Tampoco el
        pueblo antiguo, aunque cree que de haber llovido en otro punto, la DANA
        de octubre de 2024 lo habría alcanzado de nuevo. También opina que la
        situación en el pueblo mejoró con el traslado: “En el pueblo viejo era
        caer cuatro gotas y ya estábamos sufriendo porque sabíamos que el río se
        iba a salir. Aquí llueve y estamos tranquilos”.
      </p>

      <p>
        El caso de Beneixida es muy diferente al de los municipios afectados por
        la DANA de octubre de 2024, entre otras cosas por el tamaño, pues tiene
        650 habitantes, mientras que municipios como Paiporta, Catarroja,
        Alfafar, Benetússer o Picanya tienen entre 11.000 y 30.000. Su caso es
        exitoso, pero los proyectos de reconstrucción y reubicación de
        poblaciones tras una inundación no siempre prosperan.
      </p>

      <Galeriagavardaybenexida />

      <h3>Las viviendas defectuosas de Brad Pitt</h3>
      <p>
        Tras el devastador <b>huracán Katrina</b>, que asoló la costa sur de
        Estados Unidos en 2005, comenzó la reconstrucción de las ciudades
        afectadas. “En algunos sectores de Nueva Orleans se obligaba a
        <b>dejar libre la planta baja </b>para uso habitacional constante
        (dormitorios, salas de estar), según pude comprobar en el plan de
        reconstrucción que conocí hace unos años”, explica Olcina, y añade:
        “Otra cosa es que fueran construidas con mala calidad”.
      </p>

      <p>
        Es el ejemplo de uno de los proyectos de reconstrucción tras el Katrina
        que fue muy conocido por los motivos equivocados. En 2007, el actor
        estadounidense Brad Pitt <a
          href="https://www.clintonfoundation.org/press-and-news/general/press-release-president-clinton-and-cgi-u-attendees-join-brad-pitt-for-the-groun/"
          ><font color="#1155cc"><u>creó una fundación</u></font></a
        >
        con el objetivo de reconstruir
        <a href="https://graftlab.com/en/projects/make-it-right"
          ><font color="#1155cc"><u>150 viviendas</u></font></a
        >
        en un barrio de Nueva Orleans arrasado por el huracán. Las nuevas construcciones
        estarían preparadas frente a inundaciones al estar
        <b>elevadas un piso sobre el suelo</b>, usarían energía solar y se
        venderían a precios asequibles.
      </p>

      <p>
        Pero las casas acumularon varios problemas constructivos y en 2022, <b
          >sólo seis viviendas</b
        > <b>de las 109 levantadas seguían en buenas condiciones</b>, según un
        <a
          href="https://theconversation.com/how-brad-pitts-green-housing-dream-for-hurricane-katrina-survivors-turned-into-a-nightmare-175597"
          ><font color="#1155cc"><u>análisis</u></font></a
        >
        de la geógrafa Judith Keller, de la Universidad de Heidelberg (Alemania).
        Al menos dos de los residentes de estas viviendas
        <a
          href="https://www.nbcnews.com/news/us-news/brad-pitt-sued-new-orleans-residents-who-say-make-it-n907656"
          ><font color="#1155cc"><u>acabaron denunciando</u></font></a
        > a la organización por haberles vendido casas “defectuosas”.
      </p>

      <div class="contenedorimgtextoscroll">
        <img
          class="imgtxtscroll"
          src="https://files.maldita.es/maldita/uploads/2025/02/67bdbe4654e4ffile-png.png"
          alt="Gavarda y Beneixida"
        />
        <p class="piefotoscroll">
          Esta casa de Make It Right estaba vacía y tapiada en 2021. Judith
          Keller, CC BY-SA
        </p>
      </div>

      <p>
        En el proyecto de Brad Pitt en Florida, el problema fueron los defectos
        constructivos en las viviendas. Pero en otros fue la nostalgia y la
        pérdida del tejido social entre la población reubicada. Este fue el caso
        de los habitantes de
        <a
          href="https://www.google.es/maps/place/Muzaffargarh,+Pakist%C3%A1n/@32.2951815,62.8195386,5.35z/data=!4m6!3m5!1s0x393ad7ff9924fa15:0x1d3c394f0b111a2a!8m2!3d30.0736087!4d71.1804988!16zL20vMDYxeGR3?hl=es&amp;entry=ttu&amp;g_ep=EgoyMDI1MDIyNS4wIKXMDSoASAFQAw%3D%3D"
          ><font color="#1155cc"><u>Muzaffargarh</u></font></a
        >, un distrito de Pakistán que resultó muy perjudicado por las
        <a
          href="https://www.elmundo.es/elmundo/2010/08/02/internacional/1280754188.html"
          ><font color="#1155cc"><u>devastadoras inundaciones de 2010</u></font
          ></a
        >.
      </p>

      <p>
        El Gobierno regional de Punjab y una ONG organizaron la <b
          >construcción de 1.274 casas para los comunidades afectadas
        </b>por las inundaciones, que se asignaron por sorteo. Pero pasado un
        tiempo, muchos de los supervivientes vendieron o alquilaron sus casas y
        regresaron a sus pueblos originales. Según
        <a
          href="https://www.sciencedirect.com/science/article/abs/pii/S2212420923006180"
          ><font color="#1155cc"><u>un estudio</u></font></a
        >, las razones principales fueron “la
        <b>pérdida de capital social, el apego al lugar</b>, la falta de
        disponibilidad de lugares de pastoreo, la no transferencia de la
        vivienda y el aumento del coste de la vida”, indicando que factores
        psicológicos como la “nostalgia” y la “pérdida de redes sociales&quot;
        deben tenerse en cuenta en los proyectos de reubicación.
      </p>

      <p>
        Inmaculada Chordá Sampredo, segunda teniente de alcalde de Beneixida,
        explica por qué en el pueblo <b
          >no han perdido sus raíces más de 40 años después</b
        >: “La inmensa mayoría estaba decidida a no seguir allí porque tenía
        miedo, así que estábamos convencidos de que íbamos a estar mejor”.
      </p>

      <p>
        “Es verdad que a veces tienes morriña, pero intentamos hacer <b
          >actividades para que Beneixida siga siendo el pueblo que era</b
        >”, continúa. Además de la fiesta del 22 de febrero, en el municipio se
        celebra una romería cada 20 de octubre, día de ‘La pantaná’, y por
        Pascua los habitantes bajan al pinar donde estaba el pueblo viejo a
        pasar el día.
      </p>

      <p>
        “Debemos perder el miedo a la relocalización de áreas urbanas con alto
        riesgo de inundación. Lo importante es la salvaguarda de la vida humana,
        que es un mandato constitucional para las autoridades. Pero para ello
        tiene que haber
        <b>cooperación administrativa</b>”, dice Jorge Olcina.
      </p>
    </section>

    <!-- BLOQUE METODOLOGÍA Y JOURNALISM FUND -->

    <div class="metodologia-container">
      <h2 class="titulo-metodologia">
        <svg
          class="icono-metodologia"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-width="2"
            d="m21 21-3.5-3.5M17 10a7 7 0 1 1-14 0 7 7 0 0 1 14 0Z"
          />
        </svg>
        Soluciones a la inundaciones
      </h2>

      <p class="texto-metodologia">
        Este reportaje forma parte de una investigación en la que han colaborado
        
        <a href="http://Maldita.es" target="_blank">Maldita.es</a> (España), RADAR Magazine (Italia) y Eko News (República
        Checa). El proyecto se centra en analizar soluciones encontradas en
        distintos lugares del mundo frente a las inundaciones crecientes.
        
        <br><br>Este
        reportaje se ha desarrollado gracias al apoyo de <a href="https://www.journalismfund.eu/" target="_blank">Journalismfund Europe.</a>
      </p>

      <!-- Logo Journalism Fund -->
      <div class="logo-container">
        <img
          src="https://i.imgur.com/Qw2WvEg.jpeg"
          alt="Logo Journalism Fund"
        />
      </div>
    </div>
  </div>
</main>

<style>
  /* Estilo valor actual del scrolly */
  /*   mark {
    padding: 0.5em;
    position: fixed;
    top: 0;
    right: 0;
  } */
  /* Estilos generales */
  main {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin: 0 auto; /* Centra el contenido */
    padding: 0 clamp(1rem, 5vw, 3rem); /* Ajusta márgenes laterales de forma fluida */
    overflow: clip;
  }

  .spacer {
    height: 5vh; /* Ajusta la altura del espacio en blanco según sea necesario */
  }

  /* Estilos para TEXTO CUERPO */

  h2 {
    margin: 3% 20%;
    font-size: 2rem;
    line-height: 1.2;
    text-align: left;
  }

  h3 {
    margin: 3% 20%;
    font-size: 1.2rem;
    font-weight: 700;
    line-height: 1.2;
  }

  p {
    line-height: 1.6;
    margin: 3% auto;
    font-size: 17px;
    margin-left: 20%;
    margin-right: 20%;
  }

  p.piefotoscroll {
    text-align: center;
    font-size: small;
    margin-top: 0.5%;
  }

  .imgtxtscroll {
    width: 60%;
    margin: 0 auto;
    margin-left: 20%;
    margin-right: 20%;
  }

  .imgtxtscrollalerta {
    width: 20%;
    margin-left: 40%;
    margin-right: 20%;
  }

  /* Secciones con gráficos y mapas */
  .grafico {
    width: 100%;
    margin: 5% auto;
    padding: 1%;
  }

  /* BLOQUE METODOLOGÍA Y JOURNALISM FUND */
  .metodologia-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px auto;
    place-content: center;
    background-color: #cfcbcb5a;
    padding: 20px;
    border-radius: 8px;
    width: 70%;
  }
  .titulo-metodologia {
    display: flex;
    align-items: center;
    font-size: 20px;
    font-weight: bold;
  }
  .titulo-metodologia svg {
    width: 50px;
    height: 50px;
    margin-right: 5px;
  }
  .texto-metodologia {
    margin: 0 auto;
    font-size: 16px;
    line-height: 1.5;
    word-wrap: break-word;
    max-width: 100%;
  }
  .logo-container {
    text-align: center;
    margin-top: 20px;
  }
  .logo-container img {
    width: 300px;
    height: auto;
  }

  .icono-texto {
    width: 120px;
    margin: 0 45%;
  }

  /* Adaptación móvil */

  @media (max-width: 768px) {
    /*ESTILOS CUERPO MÓVIL */
    h2 {
      max-width: 90%;
      margin: 6% auto;
      font-size: 1.3rem;
      line-height: 1.3;
      text-align: left;
    }

    h3 {
      max-width: 90%;
      margin: 3% auto;
      font-size: 1rem;
      font-weight: 700;
      line-height: 1.2;
    }

    p {
      max-width: 90%;
      line-height: 1.6;
      margin: 3% auto;
      font-size: 0.9rem;
      margin-left: 5%;
      margin-right: 5%;
    }

    p.piefotoscroll {
      text-align: center;
      font-size: 0.7rem;
      margin-top: 0.5%;
    }

    .imgtxtscroll {
      width: 90%;
      margin: 0 auto;
      margin-left: 5%;
      margin-right: 5%;
    }

    .imgtxtscrollalerta {
      width: 70%;
      margin: 0 auto;
      margin-left: 15%;
      margin-right: 5%;
    }

    .icono-texto {
      width: 80px;
      margin: 0 40%;
    }

    /* Metodología */

    .metodologia-container {
      width: 80%;
    }
    .texto-metodologia {
      margin: 0 auto;
      font-size: 0.9rem;
      line-height: 1.5;
      word-wrap: break-word;
    }
  }
</style>
