<template>
  <div class="card-container">
    <div class="card">
      <h1>Marleen van Lubeek</h1>
      <h1>Webdeveloper</h1>
      <h3>www.marleen.nl</h3>
      <div class="circle"></div>
      <div class="circle"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BusinessCard',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
//@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');
@import '../assets/variables';

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.card-container {
  text-align: center;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin-top: 55vh;
  max-width: 500px;
  height: 300px;
  .card {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 300px;
    height: 200px;
    padding: 20px;
    overflow: hidden;
    background: #d4d4d4;
    border-radius: 10px;
    box-shadow: -2px 2px 0px 0px #949494,
                -10px 10px 40px 0px rgba(0, 0, 0, 0.3);
    transform: translate(0px, 0px) rotateX(30deg) rotateZ(-20deg);
    z-index: 2;
    transition: all 1s;
    &:hover {
      transform: translate(0px, -20px) rotateX(10deg) rotateZ(-20deg);;
      box-shadow: -2px 1px 0px 0px #949494,
                  -40px 40px 40px 0 rgba(0, 0, 0, 0.2);
      cursor: pointer;
    }
    h1 {
      color: $darkblue;
      font-size: 20px;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      margin-bottom: 20px;
      &:nth-of-type(2) {
        font-size: 16px;
        font-weight: 400;
        text-align: center;
      }
    }
    h3 {
      color: $darkblue;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      &:nth-of-type(2) {
        font-size: 14px;
        font-weight: 400;
      }
    }
    .circle {
      position: absolute;
      margin: auto;
      top: 10%;
      bottom: 0;
      right: -50%;
      width: 300px;
      height: 300px;
      border-radius: 50%;
      background: #c7c7c7;
      z-index: -2;
      &:nth-of-type(2) {
        width: 100px;
        height: 100px;
        top: 90%;
        right: -20%;
        z-index: -1;
        background: rgb(183, 218, 213);
      }
    }
  }
}

@media only screen and (max-width: 780px) {

  .card-container {
    .card {
      width: 250px;
      height: 150px;
      animation: hvr 5s infinite ease-in-out;
      transition: none;
      h1 {
        font-size: 18px;
        &:nth-of-type(2) {
          font-size: 14px;
        }
      }
      h3 {
        font-size: 12px;
        &:nth-of-type(2) {
          font-size: 10px;
        }
      }
      .circle {
        right: -70%;
      }
    }
  }

  @keyframes hvr {
    0% {
      box-shadow: -2px 2px 0px 0px #202020,
                  -10px 10px 40px 0px rgba(0, 0, 0, 0.3);
      transform: translate(0px, 0px) rotateX(30deg) rotateZ(-20deg);
    }
    50% {
      transform: translate(0px, -20px) rotateX(30deg) rotateZ(-20deg);;
      box-shadow: -2px 1px 0px 0px #202020,
                  -40px 40px 40px 0 rgba(0, 0, 0, 0.2);
    }
    100% {
      box-shadow: -2px 2px 0px 0px #202020,
                  -10px 10px 40px 0px rgba(0, 0, 0, 0.3);
      transform: translate(0px, 0px) rotateX(30deg) rotateZ(-20deg);
    }
  }
}
</style>
