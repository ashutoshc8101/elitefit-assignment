<script setup lang="ts">
  import { ref } from 'vue';

  import SearchPopover from "./SearchPopover.vue";

  const popoverIsShown = ref(false);

  function showPopover() {
    popoverIsShown.value = true;
  }
</script>

<template>
  <SearchPopover v-if="popoverIsShown" @onClosePopover="popoverIsShown = false" />

  <div class="header">
    <div class="container-fluid free-shipping-header">
      <div class="free-shipping-header-text">FREE SHIPPING ON ALL ORDERS</div>
    </div>

    <nav class="navbar navbar-expand-lg nav-header">
      <div class="container-fluid padding-none">
        <div class="container-fluid col-sm-2">
          <a class="navbar-brand" href="#">
            PISTONS
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
        </div>
        <div class="collapse navbar-collapse col-sm-8 justify-center" id="navbarSupportedContent">
          <ul class="navbar-nav justify-content-center mb-2 mb-lg-0 pistons-nav">
            <li class="nav-item">
              <a class="nav-link" aria-current="page" href="#">NEW</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">BRANDS</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">COLLECTIONS</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">ACCESSORIES</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#about">ABOUT</a>
            </li>
          </ul>
        </div>

        <div class="container-fluid col-sm-2 header-icons justify-content-end">
          <a @click.prevent="" href="">
            <img src="../assets/icons/shopping_cart.png" alt="search-icon" />
          </a>
          <a @click.prevent="showPopover()" href="">
            <img src="../assets/icons/search.svg" alt="search-icon" />
          </a>
        </div>
      </div>
    </nav>
  </div>
</template>

<style scoped>
  .free-shipping-header {

    width: 100%;
    height: 41px;

    background: #E3E3E3;
    /* box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25); */
  }

  .free-shipping-header-text {
    height: 19px;
    text-align: center;
    padding: 11px;

    font-style: normal;
    font-weight: 700;
    font-size: 15px;
    line-height: 19px;
    /* identical to box height */

    color: #9A9A9A;
  }

  .header {
    position: fixed;
    z-index: 100000000;
    background-color: white;
    width: 100%;
    top: 0;
  }

  .nav-header {
    padding: 28px 27px 28px 20px;
  }

  .padding-none {
    padding: 0;
  }

  .justify-center {
    justify-content: center;
  }

  .navbar-brand {
    font-family: 'Pridi', 'Oxygen', sans-serif;
    font-size: 28px;
  }

  .navbar-nav .nav-item {
    padding: 0px 15px;
  }

  .header-icons {
    display: flex;
  }

  .pistons-nav .nav-link {
    color: #000;
    text-align: center;
    font-size: 15px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
  }

  .header-icons a {
    margin-left: 14px;
  }
</style>