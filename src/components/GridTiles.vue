<template>
  <!-- content -->
  <section>
    <div class="container-fluid pistons-content">
      <div class="row row-1">
        <div class="col-lg-6 grid-item bg-color">
          <img src="../assets/images/grid-1.png" alt="grid-1" />

          <div class="grid-item-content grid-item-content-1">
            <div class="grid-item-heading">
              <!-- MADE FOR YOU -->
              <div id="box">
                <!-- <div id="c">
                </div> -->
                <div id="text">

                  <span id="t1">M</span>
                  <span id="t2">A</span>
                  <span id="t3">D</span>
                  <span id="t4">E</span>
                  <span id="t5"></span>
                  <span id="t6">F</span>
                  <span id="t7">O</span>
                  <span id="t8">R</span>
                  <span id="t9"></span>
                  <span id="t10">Y</span>
                  <span id="t11">O</span>
                  <span id="t12">U</span>
                </div>
                <div class="grid-item-text pistons-logo">
                  PISTONS
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-6 grid-item bg-color">
          <img src="../assets/images/grid-2.png" alt="grid-2" />

          <div class="grid-item-content">
            <div class="grid-item-heading">
              YOU WERE MADE TO <br /> MAKE AN IMPACT.
            </div>
            <div class="shop-pen-button">
              SHOP PENS
            </div>
          </div>
        </div>
      </div>
      <div class="row row-2">
        <div class="col-lg-6 grid-item bg-color">
          <img src="../assets/images/grid-3.png" alt="grid-3" />
          <div class="grid-item-content">
            <div class="grid-item-heading text-dark">
              MADE FOR THE BEST <br /> CHANGE MAKERS.
            </div>
            <div class="shop-pen-button bg-dark text-white">
              SHOP BRANDS
            </div>
          </div>
        </div>
        <div class="col-lg-6 grid-item bg-color ">
          <img src="../assets/images/grid-4.png" alt="grid-4" />
        </div>
      </div>
      <div class="row row-3">
        <div class="col-lg-6 grid-item bg-color">
          <img src="../assets/images/grid-5.png" alt="grid-5" />
        </div>
        <div class="col-lg-6 grid-item bg-color">
          <img src="../assets/images/grid-6.png" alt="grid-6" />
          <div class="grid-item-content">
            <div class="grid-item-heading">
              SAVOUR THE PRESENT.
            </div>
            <div class="shop-pen-button">
              SHOP MONT BLANC
            </div>
          </div>
        </div>
      </div>
      <div class="row row-4">
        <div class="col-sm-12 grid-item bg-color">
          <img class="wide-img" src="../assets/images/grid-7.png" alt="grid-2" />
          <img class="wide-img-small-screen" src="../assets/images/grid-7-sm.png" />

          <div class="grid-item-content shop-grid-item">
            <div class="grid-item-heading">
              WHERE QUALITY MEETS CLASS.
            </div>
            <div id="box2">
              <div class="text">
                <span class="t1">M</span>
                <span class="t2">A</span>
                <span class="t3">D</span>
                <span class="t4">E</span>
                <span class="t5"></span>
                <span class="t6">F</span>
                <span class="t7">O</span>
                <span class="t8">R</span>
                <span class="t9"></span>
                <span class="t10">Y</span>
                <span class="t11">O</span>
                <span class="t12">U</span>
              </div>
              <div class="grid-item-text pistons-logo">
                PISTONS
              </div>
              <div class="shop-fall-collection shop-pen-button">
              SHOP THE FALL 2023 COLLECTION
            </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
  .pistons-content {
    padding: 0px;
    /* padding-top: 140px; */
  }

  .grid-item {
    padding: 0px;
  }

  .grid-item img {
    width: 100%;
    height: 100%;
  }

  .grid-item {
    position: relative;
  }

  .grid-item .grid-item-content {
    position: absolute;
    top: 0px;
    left: 0px;
    color: #ffffff;
    text-align: center;
    width: 100%;
    margin-top: 55%;
  }

  .grid-item .grid-item-content-1 {
    margin-top: 65%;
  }

  .grid-item .grid-item-content .grid-item-heading {
    font-size: 24px;
    text-align: center;
    letter-spacing: 5.52px;
  }

  .grid-item-text.pistons-logo {
    font-family: 'Pridi', sans-serif;
    font-size: 40px;
    position: relative;
    top: -120px;
  }

  .row {
    margin-left: 0px;
    margin-right: 0px;
  }

  #box {
    /* border: 1px solid #a9703a; */
    /* height: 100px; */
    width: 100%;
    /* background: #efdcad; */
  }

  #text {
    /* transform: rotate(-55deg); */
    margin-top: 140px;
  }

  #text span {
    font-size: 40px;
    height: 440px;
    position: absolute;
    top: -120px;
  }

  #t1 {
    transform: rotate(-55deg);
  }

  #t2 {
    transform: rotate(-45deg);
  }

  #t3 {
    transform: rotate(-35deg);
  }

  #t4 {
    transform: rotate(-25deg);
  }

  #t5 {
    transform: rotate(-15deg);
  }

  #t6 {
    transform: rotate(-5deg);
  }

  #t7 {
    transform: rotate(5deg);
  }

  #t8 {
    transform: rotate(17deg);
  }

  #t9 {
    transform: rotate(25deg);
  }

  #t10 {
    transform: rotate(35deg);
  }

  #t11 {
    transform: rotate(45deg);
  }

  #t12 {
    transform: rotate(55deg);
  }

  .shop-pen-button {
    display: inline-flex;
    height: 41px;
    padding: 11px 37px 11px 38px;
    justify-content: center;
    align-items: center;
    flex-shrink: 0;

    border-radius: 50px;
    border: 4px solid #FFECC1;

    background: #FFF;

    color: #000;

    text-align: center;
    font-size: 15px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    margin-top: 18px;

    cursor: pointer;
  }

  .text-dark {
    color: black;
  }

  .grid-item .grid-item-content.shop-grid-item {
    margin-top: 10%;
  }


  #box2 {
    /* border: 1px solid #a9703a; */
    /* height: 100px; */
    width: 100%;
  }

  #box2 .text {
    margin-top: 300px;
  }

  .text span {
    font-size: 40px;
    height: 440px;
    position: absolute;
    top: 100px
  }

  .t1 {
    transform: rotate(-55deg);
  }

  .t2 {
    transform: rotate(-45deg);
  }

  .t3 {
    transform: rotate(-35deg);
  }

  .t4 {
    transform: rotate(-25deg);
  }

  .t5 {
    transform: rotate(-15deg);
  }

  .t6 {
    transform: rotate(-5deg);
  }

  .t7 {
    transform: rotate(5deg);
  }

  .t8 {
    transform: rotate(17deg);
  }

  .t9 {
    transform: rotate(25deg);
  }

  .t10 {
    transform: rotate(35deg);
  }

  .t11 {
    transform: rotate(45deg);
  }

  .t12 {
    transform: rotate(55deg);
  }

  .shop-fall-collection {
    margin-top: 0px;
    position: relative;
    z-index: 1000000;
  }

  .wide-img-small-screen {
    display: none;
  }

  @media screen and (max-width: 768px) {
    .grid-item .grid-item-content.shop-grid-item {
      margin-top: 2%;
    }

    .text span, #text span {
      font-size: 24px;
    }

    .grid-item-text.pistons-logo {
      font-size: 24px;
    }

    .grid-item .grid-item-content .grid-item-heading {
      font-size: 16px;
    }

    .shop-pen-button {
      font-size: 13px;
      padding: 9px 28px;
    }

    .wide-img {
      display: none;
    }

    .wide-img-small-screen {
      display: block;
      height: 100%;
    }

    .grid-item .grid-item-content.shop-grid-item {
      margin-top: 10%;
    }

    .grid-item .grid-item-content {
      margin-top: 45%;
    }

    .grid-item-content.shop-grid-item .grid-item-heading {
      letter-spacing: 3.68px;
    }

    #text span, .text span {
      height: 300px;
    }

    #text span {
      top: 0px;
    }

    #box2 .text {
      margin-top: 200px;
    }

    .grid-item-text.pistons-logo {
      top: -40px;
    }
  }
</style>