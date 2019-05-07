<template>
  <div class="lines">
    <div class="line1">
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
    <div class="line2">
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </div>
  </div>
</template>

<script>
export default {
name: 'BackgroundLines'
}
</script>

<style lang="scss" scoped>
@import '../assets/variables';

.lines{
  position: absolute;
  top: 0;
  height: 100%;
  margin: auto;
  width: 100%;
  z-index: -1;
  .line1{
    .line{
        position: absolute;
        height: 5px;
        top: 40%;
        background: $lightblue;
        overflow: hidden;
        box-shadow: 1px 4px 8px rgb(38, 110, 122);
        &::after{
            content: '';
            display: block;
            position: absolute;
            height: 100%;
            width: 15vh;
            top: 0%;
            left: -150%;
            background: linear-gradient(to right, rgba(255, 255, 255, 0) 0%, #9efffa 75%, $clearblue 100%);
            animation: run 10s 10s infinite;
            animation-fill-mode: forwards;
            animation-timing-function: cubic-bezier(0.45, 0.45, 0.7, 0.7);
        }
        &:nth-child(1){
        left: 0;
        width: 45%;
        border-radius: 25px;
            &::after{
                animation-delay: 0s;
            }
        }
        &:nth-child(2){
        left: 43.5%;
        width: 20%;
        border-radius: 25px;
        margin-top: -4.95%;
        transform: rotate(-30deg);
            &::after{
                animation-delay: 1.8s;
            }
        }
        &:nth-child(3){
        left: 62%;
        width: 38%;
        border-radius: 25px;
        margin-top: -9.9%;
            &::after{
                animation-delay: 3.1s;
            }
      }
    }
  }
  .line2{
    .line{
        position: absolute;
        height: 5px;
        top: 55%;
        background: $lightblue;
        overflow: hidden;
        //box-shadow: 1px 4px 8px rgb(38, 110, 122);
        &::after{
            content: '';
            display: block;
            position: absolute;
            height: 100%;
            width: 15vh;
            top: 0%;
            left: -50%;
            background: linear-gradient(to right, rgba(255, 255, 255, 0) 0%, #9efffa 75%, $clearblue 100%);
            animation: run 15s 10s infinite;
            animation-fill-mode: forwards;
            animation-timing-function: cubic-bezier(0.45, 0.45, 0.7, 0.7);
        }
        &:nth-child(1){
        left: 0;
        width: 30%;
        border-radius: 25px;
            &::after{
                animation-delay: 0s;
            }
        }
        &:nth-child(2){
        left: 28.5%;
        width: 20%;
        border-radius: 25px;
        margin-top: 4.95%;
        transform: rotate(30deg);
            &::after{
                animation-delay: 2.5s;
            }
        }
        &:nth-child(3){
        left: 47%;
        width: 53%;
        border-radius: 25px;
        margin-top: 9.9%;
            &::after{
                animation-delay: 4.3s;
            }
        }
    }
  }
}
    
@keyframes run{
  0%{
    left: -150%;
  }
  100%{
    left: 500%;
  }
}
  
// @media (max-width: 600px)
//   .wrapper
//     padding: 0 10%

</style>