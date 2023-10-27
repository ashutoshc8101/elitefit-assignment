<script setup lang="ts">

</script>

<template>
  <div class="carousel">
    <img src="../assets/images/carousel 1.jpeg" alt="carousel-1" draggable="false" />
    <img src="../assets/images/carousel 2.jpeg" alt="carousel-2" draggable="false" />
    <img src="../assets/images/carousel 3.jpeg" alt="carousel-3" draggable="false" />
    <img src="../assets/images/carousel 4.jpeg" alt="carousel-4" draggable="false" />
  </div>
</template>

<style scoped>
  .carousel img {
    width: 610px;
    height: 340px;
    margin-right: -10px;
  }

  .carousel::-webkit-scrollbar {
    display: none;
  }

  .carousel {
    overflow-x: scroll;
    white-space: nowrap;

    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  .carousel.dragging {
    cursor: grab;
    scroll-behavior: auto;
  }

  .carousel.dragging img {
    pointer-events: none;
  }

  .carousel img {
    object-fit: cover;
    user-select: none;
  }

  .carousel img:first-child {
    margin-left: 0px;
  }

  @media screen and (max-width: 768px) {
    .carousel {
      box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    }
  }
</style>