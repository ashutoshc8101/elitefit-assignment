<template>
    <div class="feedback-sticky">
    <div class="feedback-text">FEEDBACK</div>
  </div>
</template>

<style scoped>
  .feedback-sticky {
    position: fixed;
    right: 0;
    top: 35%;
    background-color: white;
    font-weight: 700;
    font-size: 25px;
    z-index: 9999;

    display: inline-flex;
    padding: 6px 7px 6px 6px;
    height: 79px;
    width: 28px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-top: 2px solid #9A9A9A;
    border-bottom: 2px solid #9A9A9A;
    border-left: 2px solid #9A9A9A;
    background: #FFF;
    cursor: pointer;
  }

  .feedback-sticky .feedback-text {
    transform: rotate(-90deg);

    text-align: center;
    font-size: 12px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 0.9px;
  }
</style>