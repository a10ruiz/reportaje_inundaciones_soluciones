<!--Galería Marjal-->
<script>
  export let images = [
    "https://files.maldita.es/maldita/uploads/2025/02/67bef0bd4b858file-jpg.jpg",
    "https://files.maldita.es/maldita/uploads/2025/02/67bef0c2449bafile-jpg.jpg",
    "https://files.maldita.es/maldita/uploads/2025/02/67bef0d095f0bfile-jpg.jpg",
    "https://files.maldita.es/maldita/uploads/2025/02/67bef0c2150a0file-jpg.jpg",
    "https://lh7-rt.googleusercontent.com/docsz/AD_4nXe8IlZau_ohGblUT2uwQ8XE52R24cJk4nLR_hmfy3wJnwtnV49P_XnIdK0eMACF0hWHFOWi-WeitYnfq85yDADAIylA6TSeaOUcJiKx8XZlCKM1doh6No7ihUU4NSd3sFL5P9vA_w?key=QvxmkaWFRlDvgClHcb-UdkgB",
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
    background: #ca4b34bd;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
  }

  @media (max-width: 768px) {
  .gallery-slider {
    flex-direction: column;
    align-items: center;
  }
  .active-image {
    width: 100%;
    max-width: 100%;
    height: auto;
    margin: 20px 0;
  }
  .nav-button {
    position: absolute;
    top: 50%;
    background: #ca4b34bd;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    transition: background 0.3s;
    font-size: 18px;
  }

  .nav-button.left {
    left: 3.3%;
  }
  .nav-button.right {
    right: 3.3%;
  }
  .image-counter {
    position: absolute;
    bottom: 10%;
    left: 50%;
    transform: translateX(-50%);
    background: #ca4b34bd;
    color: white;
    padding: 5px 10px;
    border-radius: 5px;
    font-size: 16px;
  }
}
</style>