<script setup lang="ts">
  import { ref } from "vue";

  const testimonials = ref([
    {
      "name": "Alex P.",
      "message": "I stumbled upon this shop, and their selection blew me away. The user-friendly website made my shopping experience a breeze!",
      "image": "https://i.ibb.co/vmYY6tY/img1.png"
    },
    {
      "name": "Emily S.",
      "message": "The checkout process was seamless, and the responsive design worked flawlessly on my mobile device. I'll definitely be coming back!",
      "image": "https://i.ibb.co/k29V4KN/img2.png"
    },
    {
      "name": "David R.",
      "message": "Their site's intuitive navigation made finding the perfect pen a joy. Five stars for both their products and web design!",
      "image": "https://i.ibb.co/Mcz1SWT/img3.png"
    },
    {
      "name": "Lisa M.",
      "message": "I appreciate the attention to detail in both their pens and website. A visually stunning and user-focused online shop.",
      "image": "https://i.ibb.co/94fW8xZ/img4.png"
    }
  ]);
</script>

<template>
  <section class="testimonials">
    <div class="testimonials-heading">TESTIMONIALS</div>

    <div class="testimonial-list">
      <div class="container">
        <div class="row testimonial-row">
          <div v-for="(testimonial, index) in testimonials" :key="index" class="col-sm-3">
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

  .row.testimonial-row {
    flex-grow: 1 1 1 1;
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
</style>