<script setup lang="ts">
  import { ref } from "vue";

  const testimonials = ref([]);

  try {
    // https://elitefit4you.com/test-api/testimonials.json is not
    // fetchable by javascript client as CORS is not enabled for this endpoint.
    // Hence, testimonials.json is self hosted and fetched.
    const response = await fetch('/testimonials.json');

    testimonials.value = Object.freeze(await response.json());
  } catch (e) {
    console.error(e);
  }
</script>

<template>
  <section class="testimonials">
    <div class="testimonials-heading">TESTIMONIALS</div>

    <div class="testimonial-list">
      <div class="container">
        <div class="row testimonial-row">
          <div v-for="(testimonial, index) in testimonials" :key="index" class="testimonial-container col-lg-3">
            <div class="testimonial">
              <img :src="testimonial['image']" alt="alex-p" />
              <div class="testimonial-author">{{ testimonial['name'] }}</div>

              <div class="text-overlay">
                "{{ testimonial['message'] }}"
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
  .testimonials {
    padding: 38px 105px 83px 105px;
  }

  .testimonials-heading {
    color: #000;
    text-align: center;
    font-size: 36px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 7.92px;
  }

  .testimonial-list {
    margin-top: 109px;
  }

  .testimonial {
    position: relative;
    height: 277px;
    border-radius: 20px;
    padding: 0px;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  }

  .testimonial img {
    height: 100%;
    width: 100%;
    border-radius: 20px;
  }

  .testimonial .testimonial-author {
    position: absolute;
    top: 0;
    text-align: center;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #FFF;
    text-align: center;
    font-size: 36px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
  }

  .testimonials {
    background-color: white;
    position: relative;
    z-index: 10;
  }

  .testimonial .text-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1000;
    padding: 80px 27px;
    background-color: black;
    border-radius: 20px;
    color: white;
    opacity: 0;
  }

  .testimonial .text-overlay:hover {
    opacity: 1;
    transition: opacity 0.2s;
  }

  @media screen and (max-width: 922px) {

    .testimonial-list {
      margin-top: 20px;
    }

    .testimonials {
      padding: 20px;
    }

    .testimonial-container {
      margin: 25px 0px;
      padding: 0px;
    }


    .testimonials-heading {
      font-size: 24px;
    }

    .testimonial .testimonial-author {
      font-size: 24px;
    }

    .text-overlay {
      font-size: 14px;
    }
  }
</style>