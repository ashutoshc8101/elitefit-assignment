<script lang="ts">
  export default {
    props: ['popoverIsShown'],
    methods: {
      closePopover() {
        this.$emit('onClosePopover');
      }
    }
  }
</script>

<template>
  <div class="search-popover" :class="{ hidden: !popoverIsShown }">
    <div class="search-header">
      <img src="../assets/icons/Close.png" @click="closePopover()" />
    </div>
    <div class="search-content">
      <input class="search-input" type="text" />
      <div class="search-button">Search</div>
    </div>
  </div>
</template>

<style scoped>
  .search-popover {
    max-width: 436px;
    width: 100%;
    background-color: #FFF;
    padding: 8px;
    display: inline-block;
    position: fixed;
    right: 0px;
    top: 140px;
    z-index: 1000000000;
    transition: right 0.3s;
  }

  .search-popover.hidden {
    right: -450px;
  }

  .search-popover .search-input {
    margin: 5px 0px;
    height: 33px;
    border-radius: 50px;
    border: 1px solid #000;
    background: #FFF;
    outline: none;
    padding: 0px 10px;
    flex-grow: 1;
    margin-right: 10px;
  }

  .search-button {
    border-radius: 50px;
    border: 3px solid #FFECC1;
    display: inline-flex;
    height: 41px;
    padding: 11px 32px;
    justify-content: center;
    align-items: center;
    flex-shrink: 0;
    background: #000;
    color: #FFF;

    text-align: center;
    font-size: 15px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    cursor: pointer;
  }

  .search-header {
    text-align: right;
  }

  .search-header img {
    cursor: pointer;
  }

  .search-content {
    padding: 0px 32px;
    margin-bottom: 21px;
    display: flex;
    justify-content: space-between;
  }

  @media screen and (max-width: 768px) {
    .search-popover {
      right: 0px;
      top: 105px;
      transition: top 0.3s;
    }

    .search-popover.hidden {
      top: -110px;
    }
  }
</style>