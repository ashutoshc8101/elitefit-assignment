<script setup lang="ts">
  import { ref } from 'vue';

  import SearchPopover from "./SearchPopover.vue";

  const emit = defineEmits(['toggleOverlay']);

  const popoverIsShown = ref(false);
  const navMenuIsShown = ref(false);

  function showPopover() {
    popoverIsShown.value = true;
  }

  function showNavMenu() {
    emit('toggleOverlay');
    navMenuIsShown.value = true;
  }

  function hideNavMenu() {
    emit('toggleOverlay');
    navMenuIsShown.value = false;
  }
</script>

<template>
  <SearchPopover :popoverIsShown="popoverIsShown" @onClosePopover="popoverIsShown = false" />

  <div class="header">
    <div class="container-fluid free-shipping-header">
      <div class="free-shipping-header-text">FREE SHIPPING ON ALL ORDERS</div>
    </div>

    <nav class="navbar navbar-expand-lg nav-header">
      <div class="container-fluid padding-none">
        <div class="container-fluid col-2">
          <a class="navbar-brand" href="#">
            PISTONS
          </a>
        </div>
        <div class="col-8 small-device-placeholder" />
        <div class="col-sm-8 justify-center navbar-menu-container" :class="{ close: !navMenuIsShown }" id="navbarSupportedContent">
          <div className="navmenu-header">
            <img src="../assets/icons/Close.png" @click.prevent="hideNavMenu()" />
          </div>
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

        <div class="container-fluid col-2 header-icons justify-content-end">
          <a @click.prevent="" href="">
            <img src="../assets/icons/shopping_cart.png" alt="search-icon" />
          </a>
          <a @click.prevent="showPopover()" href="">
            <img src="../assets/icons/search.svg" alt="search-icon" />
          </a>

          <img @click.prevent="showNavMenu()" class="nav-dropdown-icon" src="../assets/icons/bars.png" alt="bread" />
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
    z-index: 10000000;
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

  .nav-dropdown-icon {
    display: none;
  }

  .navmenu-header {
    display: none;
  }

  .small-device-placeholder {
    display: none;
  }

  @media screen and (max-width: 992px) {
    .nav-dropdown-icon {
      display: block;
      margin-left: 16px;
    }

    .navmenu-header {
      display: flex;
      justify-content: flex-end;
      padding: 10px 10px 5px;
    }

    .navbar-menu-container {
      display: inline-block;
      position: absolute;
      top: 0px;
      right: 0px;
      border: 1px solid #9A9A9A;
      background: #FFF;
      width: 254px;
      padding-bottom: 10px;
      transition: right 0.3s;
      z-index: 1000000;
    }

    .navbar-menu-container.close {
      right: -260px;
    }

    .navbar-expand-lg .navbar-nav {
      display: block;
    }

    .small-device-placeholder {
      display: block;
    }
  }

  @media screen and (max-width: 768px) {
    .navbar-brand {
      padding: 0px;
      height: 19px;
      font-size: 19px;
    }

    .header-icons img {
      width: 24px;
      height: 24px;
    }

    .nav-header {
      padding: 18px 12px;
    }

    .free-shipping-header-text {
      font-size: 10px;
    }
  }
</style>