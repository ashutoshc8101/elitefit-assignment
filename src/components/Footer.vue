<template>
  <section class="footer">
    <div class="piston-logo" href="#">
      PISTONS
    </div>

    <div class="stay-connected">
      STAY CONNECTED
    </div>

    <div class="social-icons">
      <img src="../assets/icons/facebook.png" alt="facebook" />
      <img src="../assets/icons/youtube.png" alt="youtube" />
      <img src="../assets/icons/instagram.png" alt="instagram" />
      <img src="../assets/icons/twitter.png" alt="twitter" />
      <img src="../assets/icons/message.png" alt="email" />
    </div>
  </section>
</template>

<style scoped>
  .footer {
    padding: 26px;
    background-color: black;
  }

  .piston-logo {
    color: #FFF;
    font-family: Pridi;
    font-size: 40px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    text-align: center;
  }

  .stay-connected {
    color: #FFF;
    text-align: center;
    font-family: Oxygen;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    letter-spacing: 5.28px;
    margin: 25px 0px;
  }

  .social-icons {
    display: flex;
    width: 100%;
    justify-content: center;
  }

  .social-icons img {
    margin: 15px;
    cursor: pointer;
  }
</style>