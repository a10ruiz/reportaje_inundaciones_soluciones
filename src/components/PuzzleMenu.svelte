<script>
    import { onMount, onDestroy } from "svelte";
    import { writable } from "svelte/store";

    // Variable para controlar si el menú se encoge
    let isShrunk = writable(false);
    let activeSection = writable(null);

    // Detectar el scroll y cambiar el tamaño del menú
    function handleScroll() {
        const parte1 = document.getElementById("parte1");
        if (!parte1) return;

        const rect = parte1.getBoundingClientRect();

        // Si parte1 ya ha sido pasada (su borde superior está fuera de la vista)
        if (rect.top <= 0) {
            isShrunk.set(true);
        } else {
            isShrunk.set(false);
        }

        // Detectar en qué sección estamos
        const sections = document.querySelectorAll("section");
        let currentSection = null;
        sections.forEach((section) => {
            const rect = section.getBoundingClientRect();
            if (rect.top <= 150 && rect.bottom >= 150) {
                currentSection = section.id;
            }
        });
        activeSection.set(currentSection);
    }

    onMount(() => {
        window.addEventListener("scroll", handleScroll);
    });

    onDestroy(() => {
        window.removeEventListener("scroll", handleScroll);
    });
</script>

<div class="puzzle-menu" class:shrunk={$isShrunk}>
    <a href="#parte1" class="puzzle" class:active={$activeSection === "parte1"}>
        <svg viewBox="0 0 533.33 533.33" xmlns="http://www.w3.org/2000/svg"
            ><script xmlns=""></script>
            <path
                d="m123.1 125.62l0.125 96.938s1.0792 22.686 20.594 18.906c15.856-3.0711 10.233-24.878 22.688-25.844 2.8742-0.22286 6.7148 0.67577 12 3.1562 10.909 9.0951 16.003 26.144 16.562 41.344 0.20657 5.611-0.2833 10.888-1.25 15.5-0.024811 0.20468-0.067291 0.42017-0.09375 0.625-1.6939 13.114-6.7618 26.418-15.969 34.094-28.188 13.229-15.173-18.908-34.688-22.688-14.218-2.7539-18.61 8.4783-19.969 14.812v102.91l98.094-0.78125s22.686-1.0792 18.906-20.594c-3.7798-19.515-35.886-6.4998-22.656-34.688 9.0951-10.909 26.113-16.003 41.312-16.562 5.611-0.20657 10.888 0.2833 15.5 1.25 0.20468 0.024811 0.4202 0.067291 0.625 0.09375 13.114 1.6939 26.449 6.7618 34.125 15.969 13.229 28.188-18.908 15.173-22.688 34.688-3.7798 19.515 18.906 20.594 18.906 20.594l97.188 0.0312v-102.09c1.3864-6.3521 5.8027-17.456 19.938-14.719 19.515 3.7798 6.4998 35.917 34.688 22.688 9.2069-7.6759 14.275-21.011 15.969-34.125 0.026459-0.20483 0.068939-0.38907 0.09375-0.59375 0.9667-4.6121 1.4566-9.889 1.25-15.5-0.55954-15.199-5.6533-32.249-16.562-41.344-28.188-13.229-15.173 18.908-34.688 22.688-19.515 3.7798-20.594-18.906-20.594-18.906l-0.0938-97.844-97.344 0.71875s-22.686 1.0792-18.906 20.594c3.7798 19.515 35.917 6.4998 22.688 34.688-9.0951 10.909-26.144 16.003-41.344 16.562-5.6109 0.20656-10.888-0.2833-15.5-1.25-0.20468-0.024811-0.42018-0.067291-0.625-0.09375-13.114-1.6939-26.418-6.7618-34.094-15.969-13.229-28.188 18.876-15.173 22.656-34.688 3.7201-19.207-17.964-20.525-18.656-20.562h-98.188z"
            />
        </svg>
        <p class="uno">Antes</p>
        <p class="dos">avisar: <span>El modelo de Japón </span></p>
    </a>
    <a href="#parte2" class="puzzle" class:active={$activeSection === "parte2"}>
        <svg
            viewBox="0 0 533.33 533.33"
            xmlns="http://www.w3.org/2000/svg"
            style="rotate: 90deg;"
            ><script xmlns=""></script>
            <path
                d="m53.141 271.84c0.55954 15.199 5.6533 32.249 16.562 41.344 28.188 13.229 15.173-18.908 34.688-22.688 19.515-3.7798 20.594 18.906 20.594 18.906v97.75l96.938-0.125s22.686-1.0792 18.906-20.594c-3.0711-15.856-24.878-10.233-25.844-22.688-0.22286-2.8742 0.67577-6.7148 3.1562-12 9.0951-10.909 26.144-16.003 41.344-16.562 5.611-0.20657 10.888 0.2833 15.5 1.25 0.20468 0.024811 0.42017 0.067291 0.625 0.09375 13.114 1.6939 26.418 6.7618 34.094 15.969 13.229 28.188-18.908 15.173-22.688 34.688-2.7539 14.218 8.4783 18.61 14.812 19.969h102.91v-101.59c1.2183-6.2012 5.4891-18.241 20.125-15.406 19.515 3.7798 6.4998 35.886 34.688 22.656 9.207-7.676 14.275-20.979 15.969-34.094 0.026489-0.20483 0.068939-0.42032 0.09375-0.625 0.9667-4.6121 1.4566-9.8891 1.25-15.5-0.55954-15.199-5.6533-32.249-16.562-41.344-28.188-13.229-15.173 18.908-34.688 22.688-19.515 3.7798-20.594-18.906-20.594-18.906l-0.2812-97.188s-98.25 0.62501-98.25 0.62499c0 0-22.686 1.0792-18.906 20.594 3.7798 19.515 35.917 6.4998 22.688 34.688-9.0951 10.909-26.144 16.003-41.344 16.562-5.6109 0.20656-10.888-0.28328-15.5-1.25-0.20468-0.024811-0.42018-0.067276-0.625-0.09375-13.114-1.6939-26.418-6.7618-34.094-15.969-2.4805-5.2852-3.3791-9.1258-3.1562-12 0.96571-12.455 22.741-6.8319 25.812-22.688 3.5267-18.208-15.34-20.261-17.969-20.469h-98.406v102.16c-1.4819 6.4056-5.9919 16.964-19.844 14.281-19.515-3.7798-6.4998-35.886-34.688-22.656-9.2069 7.676-14.275 20.979-15.969 34.094-0.026459 0.20483-0.068939 0.4203-0.09375 0.62502-0.9667 4.612-1.4566 9.889-1.25 15.5z"
                stroke-width="3.585"
            />
        </svg>
        <p class="uno">Durante</p>
        <p class="dos">
            contar con infraestructuras: <span
                >Experiencias en el Ebro y Alicante</span
            >
        </p>
    </a>
    <a href="#parte3" class="puzzle" class:active={$activeSection === "parte3"}>
        <svg
            viewBox="0 0 533.33 533.33"
            xmlns="http://www.w3.org/2000/svg"
            style="rotate: 180deg;"
            ><script xmlns=""></script>
            <path
                d="m123.1 125.62l0.125 96.938s1.0792 22.686 20.594 18.906c15.856-3.0711 10.233-24.878 22.688-25.844 2.8742-0.22286 6.7148 0.67577 12 3.1562 10.909 9.0951 16.003 26.144 16.562 41.344 0.20657 5.611-0.2833 10.888-1.25 15.5-0.024811 0.20468-0.067291 0.42017-0.09375 0.625-1.6939 13.114-6.7618 26.418-15.969 34.094-28.188 13.229-15.173-18.908-34.688-22.688-14.218-2.7539-18.61 8.4783-19.969 14.812v102.91l98.094-0.78125s22.686-1.0792 18.906-20.594c-3.7798-19.515-35.886-6.4998-22.656-34.688 9.0951-10.909 26.113-16.003 41.312-16.562 5.611-0.20657 10.888 0.2833 15.5 1.25 0.20468 0.024811 0.4202 0.067291 0.625 0.09375 13.114 1.6939 26.449 6.7618 34.125 15.969 13.229 28.188-18.908 15.173-22.688 34.688-3.7798 19.515 18.906 20.594 18.906 20.594l97.188 0.0312v-102.09c1.3864-6.3521 5.8027-17.456 19.938-14.719 19.515 3.7798 6.4998 35.917 34.688 22.688 9.2069-7.6759 14.275-21.011 15.969-34.125 0.026459-0.20483 0.068939-0.38907 0.09375-0.59375 0.9667-4.6121 1.4566-9.889 1.25-15.5-0.55954-15.199-5.6533-32.249-16.562-41.344-28.188-13.229-15.173 18.908-34.688 22.688-19.515 3.7798-20.594-18.906-20.594-18.906l-0.0938-97.844-97.344 0.71875s-22.686 1.0792-18.906 20.594c3.7798 19.515 35.917 6.4998 22.688 34.688-9.0951 10.909-26.144 16.003-41.344 16.562-5.6109 0.20656-10.888-0.2833-15.5-1.25-0.20468-0.024811-0.42018-0.067291-0.625-0.09375-13.114-1.6939-26.418-6.7618-34.094-15.969-13.229-28.188 18.876-15.173 22.656-34.688 3.7201-19.207-17.964-20.525-18.656-20.562h-98.188z"
            />
        </svg>
        <p class="uno">Después</p>
        <p class="dos">
            legislar y... ¿reubicar?: <span>De EEUU a Beneixida</span>
        </p>
    </a>
</div>

<style>
    .puzzle-menu {
        position: sticky;
        top: 0;
        margin: 0 auto;
        width: 65%;
        color: #4a90e2;
        background-color: rgba(255, 255, 255, 0.8);
        backdrop-filter: blur(6px);
        z-index: 999;
        display: flex;
        justify-content: space-around;
        align-items: center;
        gap: 10%;
        border-radius: 7px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        transition: all 0.5s ease-in-out; /* Transición más suave */
        transform-origin: top center;
        }

    .puzzle-menu p {
        margin: 2%;
        padding: auto;
        border-radius: 8px;    
        transition: opacity 0.4s ease-in-out, visibility 0.4s ease-in-out;
    }

    /* Estilos individuales */
    .puzzle-menu p.uno {
        font-size: 0.8rem;
        color: #333;
        background: rgba(200, 200, 200, 0.3); /* Gris claro translúcido */
        padding: 4%;
        text-align: center;
        white-space: nowrap;
    }

    .puzzle-menu p.dos {
        font-size: 0.85rem;
        font-variant: small-caps;
        font-weight: 600;
        color: #444;
        text-align: center;
        line-height: 1.1;
    }

    .puzzle-menu p.dos span {
        font-size: 0.8rem;
        font-variant: normal;
        font-style: normal;
       
    }

    .puzzle-menu.shrunk {
        transform: scale(0.5);
        width: 75%;
        height: fit-content;
        top: 10%;
        gap: 10%;
        padding: 1% 5%;
    }

    .puzzle-menu.shrunk .puzzle {
        margin: 5px;
    }

    .puzzle-menu.shrunk p {
        display: none;
    }

    .puzzle {
        flex: 1;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        cursor: pointer;
        text-decoration: none;
        color: black;
        transition: all 0.3s ease-in-out;
        border: 2px solid #909090; /* Borde azul */
        border-radius: 10px; /* Esquinas redondeadas */
        padding: 2%; /* Espacio interno para que el borde no esté pegado */
        transition: transform 0.3s ease-in-out, border-color 0.3s ease-in-out;
    }

    .puzzle.active {
        border-color: #078484; /* Cambio de color cuando está activo */
    }

    .puzzle svg {
        width: 100px;
        height: 100px;
        transition: fill 0.3s ease;
    }

    .puzzle path {
        fill: #ca4a34; /* Color por defecto cuando NO está activo */
        transition: fill 0.3s ease;
    }

    .puzzle.active path {
        fill: #078484;
    }

    /*Hover*/
    .puzzle-menu svg:hover {
        transform: scale(1.2);
        transition: transform 0.2s ease;
    }

    .puzzle:hover {
        border-color: #ca4a34;
    }

    .puzzle.active:hover {
        border-color: #078484;
    }

    @media (max-width: 768px) {
  .puzzle-menu {
    position: sticky;
    top:5%;
    flex-direction: row;
    gap: 5px;
    padding: 1% 1%;
    width: 99%;
    height: fit-content;
  }
  .puzzle {
    flex: 1;
    margin: 5px;
    height: 180px;
    width: 100px;
  }

  .puzzle svg {
    width: 65px;
    height: 65px;
  }
  .puzzle p {
    font-size: 0.8rem;
  }

  .puzzle-menu.shrunk {
      width: 95%;
      height: fit-content;
      border-radius: 10px;
      top: 2%;
      padding: 3% 10%;
  }
  .puzzle-menu.shrunk .puzzle {
    width: 100%;
    height: fit-content;
    border: 4px solid #ca4a34;
    border-radius: 0;
  }

  .puzzle-menu.shrunk .puzzle.active {
    border: 4px solid #078484;
  }

  .puzzle-menu.shrunk .puzzle svg {
    width: 75px;
    height: 75px;
  }

  .puzzle-menu p.uno {
    font-size: 0.7rem;
  }

  .puzzle-menu p.dos {
    font-variant: small-caps;
    font-size: 0.75rem;
  }

  .puzzle-menu p.dos span {
    font-size: 0.7rem;
  }


}
</style>
