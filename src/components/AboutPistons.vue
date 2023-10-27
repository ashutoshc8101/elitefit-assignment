<script setup lang="ts">
  import ImageCarousel from "./ImageCarousel.vue";
</script>

<template>
  <section id="about" class="about-pistons container-fluid">
    <div class="row">
      <div class="col-lg-6 image-carousel-container">
        <ImageCarousel />
      </div>
      <div class="col-lg-6 about-text">
        <div class="about-pistons-heading">ABOUT PISTONS</div>
        <div class="about-pistons-text">
          Established in 1897, our beloved fountain pen haven, 'PISTONS,' has been a haven for pen enthusiasts for generations. With a century-long dedication to fine writing instruments, we've bridged tradition and modernity, offering a curated selection of vintage and contemporary fountain pens. Our little shop, nestled in the heart of town, continues to inspire a love for the art of writing, connecting past and present through the timeless elegance of ink on paper.
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .about-pistons {
    padding: 90px;
    padding-top: 160px;
  }

  .about-pistons .about-pistons-heading {
    color: #000;
    padding: 40px 80px 0px 80px;
    font-size: 36px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 7.92px;
    margin-bottom: 17px;
  }

  .about-pistons-text {
    color: #000;
    font-size: 15px;
    font-style: normal;
    font-weight: 400;
    line-height: 158.27%;
    padding: 0px 80px;
    text-align: left;
  }

  @media screen and (max-width: 768px) {
    .about-pistons .about-pistons-heading {
      padding: 0px;
      margin-top: 42px;
      font-size: 26px;
    }

    .about-pistons-text {
      padding: 0px;
      font-size: 13px;
    }

    .about-pistons {
      margin-top: 10px;
      padding: 30px 12px 30px 30px;
    }

    .row > .image-carousel-container {
      padding: 0px;
    }
  }
</style>