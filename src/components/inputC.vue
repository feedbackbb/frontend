<template>
<div class="intputC">
  <p class="t1 jello-vertical">Welcome to</p>
  <p class="t2 jello-vertical"> the washing machine service.</p>
  <p class="t3">คุณมียอดจำนวน {{coin}} บาท</p>

  <button class="button-7" role="button" @click="topup">เติมเงิน</button>
</div>
</template>

<script>
export default {
    name:"inputC",
    data() {
      return {
        coin:0
      }
    },
    methods: {
      topup(){
        this.coin=30
      }
    },

}
</script>

<style>
 .t1{
  font-size: 10.5rem;
  color: #555;
 }

 .t2{
  font-size: 5.5rem;
  color: #555;
 }

 .t3 {
    font-size: 2rem;
    color: #555;
    margin: 100px 0 20px 0;
  }

 .intputC{
  height: 100vh;
  background-color: #fff;
  display: flex;
  flex-direction: column;
  width: 50vw;
  align-items: center;
  justify-content: center;
 }

/* CSS */
.button-7 {
  margin-top: 20px;
  background-color: #0095ff;
  border: 1px solid transparent;
  border-radius: 3px;
  box-shadow: rgba(255, 255, 255, .4) 0 1px 0 0 inset;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-family: -apple-system,system-ui,"Segoe UI","Liberation Sans",sans-serif;
  font-size: 2rem;
  font-weight: 400;
  line-height: 1.15385;
  margin: 0;
  outline: none;
  padding: 8px .8em;
  position: relative;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  vertical-align: baseline;
  white-space: nowrap;
}

.button-7:hover,
.button-7:focus {
  background-color: #07c;
}

.button-7:focus {
  box-shadow: 0 0 0 4px rgba(0, 149, 255, .15);
}

.button-7:active {
  background-color: #0064bd;
  box-shadow: none;
}

@media only screen and (max-width: 1440px) {
  .t1{
  font-size: 8.5rem;
  color: #555;
 }

 .t2{
  font-size: 2.5rem;
  color: #555;
 }

 .t3 {
    font-size: 1rem;
    color: #555;
    margin: 100px 0 20px 0;
  }
}
@media only screen and (max-width: 1024px) {
  
  .t1{
  font-size: 4.5rem;
  color: #555;
 }

 .t2{
  font-size: 1.5rem;
  color: #555;
 }

 .t3 {
    font-size: 1rem;
    color: #555;
    margin: 100px 0 20px 0;
  }
}
@media only screen and (max-width: 768px) {
  .intputC{
  width: 100vw;
 }
}
 @media only screen and (max-width: 425px) {
   .t1{
  font-size: 3.5rem;
  color: #555;
 }
  img{
    height: 400px;
  }
 }
  
/* effect */
.jello-vertical {
	animation: jello-vertical 0.9s both;
}
/* ----------------------------------------------
 * Generated by Animista on 2023-3-21 19:54:41
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation jello-vertical
 * ----------------------------------------
 */
@keyframes jello-vertical {
  0% {
    transform: scale3d(1, 1, 1);
  }
  30% {
    transform: scale3d(0.75, 1.25, 1);
  }
  40% {
    transform: scale3d(1.25, 0.75, 1);
  }
  50% {
    transform: scale3d(0.85, 1.15, 1);
  }
  65% {
    transform: scale3d(1.05, 0.95, 1);
  }
  75% {
    transform: scale3d(0.95, 1.05, 1);
  }
  100% {
    transform: scale3d(1, 1, 1);
  }
}

</style>
