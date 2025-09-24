<!--Galería Marjal-->
<script>
    export let images = [
      "https://files.maldita.es/maldita/uploads/2025/02/67beffc8da104file-jpg.jpg",
      "https://files.maldita.es/maldita/uploads/2025/02/67beffc762900file-jpg.jpg",
      "https://files.maldita.es/maldita/uploads/2025/02/67beffc938f39file-jpg.jpg",
      "https://files.maldita.es/maldita/uploads/2025/02/67beffc8e0f44file-jpg.jpg",
      "https://files.maldita.es/maldita/uploads/2025/02/67beffc960970file-jpg.jpg",
      "https://files.maldita.es/maldita/uploads/2025/02/67beffc95cb4cfile-jpg.jpg"
    ];
  
    let currentIndex = 0;
  
    function prev() {
      currentIndex = (currentIndex - 1 + images.length) % images.length;
    }
  
    function next() {
      currentIndex = (currentIndex + 1) % images.length;
    }
  </script>
  
  <div class="gallery-slider">
    <button class="nav-button left" on:click={prev}>&lt;</button>
    <img src={images[currentIndex]} alt="Galería" class="active-image" />
    <button class="nav-button right" on:click={next}>&gt;</button>
    <div class="image-counter">{currentIndex + 1} / {images.length}</div>
  </div>
  
  <style>
    .gallery-slider {
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .active-image {
      width: 60%;
      max-width: 750px;
      display: block;
    }
    .nav-button {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: #ca4b34bd;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }
    .nav-button.left { left: 20.7%; }
    .nav-button.right { right: 20.7%; }
    .nav-button:hover {
      background: #ca4a34;
      transform: scale(1);
    }
    .nav-button:active {
      transform: scale(0.9);
    }
    .image-counter {
      position: absolute;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      background: #ca4b34bd;
      color: white;
      padding: 5px 10px;
      border-radius: 5px;
    }
  </style>