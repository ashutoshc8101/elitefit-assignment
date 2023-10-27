<script lang="ts">
  export default {
    methods: {
      closePopover() {
        this.$emit('onClosePopover');
      }
    }
  }
</script>

<template>
  <div class="search-popover active">
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
    width: 436px;
    background-color: #FFF;
    padding: 8px;
    display: inline-block;
    position: absolute;
    right: 0;
    top: 140px;
    z-index: 100000;
    display: none;
  }

  .search-popover.active {
    display: block;
  }

  .search-popover .search-input {
    margin: 5px 0px;
    height: 33px;
    width: 226px;
    border-radius: 50px;
    border: 1px solid #000;
    background: #FFF;
    outline: none;
    padding: 0px 10px;
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
</style>