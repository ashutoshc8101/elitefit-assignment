<script setup lang="js">
  import { ref } from 'vue';

  let isDown = false;
  let startX;
  let scrollLeft;
  // const slider = document.querySelector('.items');
  const slider = ref(null);

  const end = () => {
    isDown = false;
    slider.value.classList.remove('active');
  }

  const start = (e) => {
    // console.log('drag start');
    isDown = true;
    slider.value.classList.add('active');
    startX = e.pageX || e.touches[0].pageX - slider.value.offsetLeft;
    scrollLeft = slider.value.scrollLeft;
  }

  const move = (e) => {
    // console.log('drag move', isDown);
    if(!isDown) return;

    e.preventDefault();
    const x = e.pageX || e.touches[0].pageX - slider.value.offsetLeft;
    const dist = (x - startX);
    slider.value.scrollLeft = scrollLeft - dist;
  }
</script>

<template>
  <div class="carousel-container">
    <div class="carousel">
      <ul class="items" ref="slider" @mousedown="start" @touchstart="start" @mousemove="move"
          @touchmove="move" @mouseleave="end" @mouseup="end" @touchend="end">
        <img class="item" src="../assets/images/carousel 1.jpeg" alt="carousel-1" draggable="false" />
        <img class="item" src="../assets/images/carousel 2.jpeg" alt="carousel-2" draggable="false" />
        <img class="item" src="../assets/images/carousel 3.jpeg" alt="carousel-3" draggable="false" />
        <img class="item" src="../assets/images/carousel 4.jpeg" alt="carousel-4" draggable="false" />
      </ul>
    </div>
  </div>
</template>

<style scoped>
  .carousel-container {
    display: flex;
    justify-content: center;
  }

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

  .carousel img {
    object-fit: cover;
    user-select: none;
  }

  .carousel {
    position: relative;
    max-width: 600px;
    text-align: center;
  }


  .items {
    position: relative;
    width: 100%;
    overflow: hidden;
    white-space: nowrap;
    font-size: 0;
    cursor: pointer;
    padding: 0px;
    margin: 0px;
  }

  .items.active {
    cursor: grab;
  }

  .item {
    display: inline-block;
    margin-left: 0px;
    user-select: none;

    width: 50%;
    height: 130px;
    font-size: 33px;
    font-weight: bold;
    line-height: 130px;
  }


  @media screen and (min-width: 500px) {

    .item {
      width: 33%;
    }
  }

  @media screen and (min-width: 800px) {

    .item {
      width: 25%;
    }
  }

  @media screen and (min-width: 1200px) {

    .wrapper {
      margin-left: 0px;
    }

    .item {
      width: 20%;
    }
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