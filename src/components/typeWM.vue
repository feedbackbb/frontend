<template>
<div class="hide">

  <div v-show="!hide" class="cdown">
    <p class="t2r">ระยะเวลาทำความสะอาด</p>
    <countdown/>
  </div>

  <div v-if="hide" class="typeWM">
    <p class="t1r">โปรดเลือกชนิดของเครื่องซักผ้า</p>
    <div>
      <select v-model="selected">
        <option v-for="index in productWM" :value="index.imgWM" >
          {{ index.productName }}
        </option>
      </select> 
      <!-- <div>Selected: {{ selected }}</div> -->
    </div>
    <div class="imgBox">
      <img :src=" selected">
    </div>

    <button class="button-7" role="button" @click="hide = !hide">เลือก</button>
  </div>
</div>


</template>

<script>
import countdown from '@/components/countdown.vue'
export default {
    name:"typeWM",
     components:{
      countdown
     },
    data() {
      return {
        hide: true,
        selected:require("../assets/01.png"),
        productWM:
        [
          {
            productID:"01",
            productName:"เครื่องซักผ้า WashTower",
            imgWM:require("../assets/01.png"),
          },
          {
            productID:"02",
            productName:"เครื่องซักผ้าฝาหน้า",
            imgWM:require("../assets/02.png"),
          },
          {
            productID:"03",
            productName:"เครื่องซักผ้าฝาบน",
            imgWM:require("../assets/03.png"),
          },
          {
            productID:"04",
            productName:"เครื่องซักผ้าสองถัง",
            imgWM:require("../assets/04.png"),
          },
        ],
      }
    },
    methods: {

    },

}
</script>

<style>
.cdown{
  height: 100vh;
  background-color: #fff;
  display: flex;
  flex-direction: column;
  width: 50vw;
  align-items: center;
  justify-content: center;
}

img{
  height: 800px;
}

.t1r{
  font-size: 3rem;
  color: #fff;
  margin: 60px 0 20px 0;
}

.t2r{
  font-size: 3rem;
  color: #555;
  margin: 60px 0 20px 0;
}

select{
    font-size: 32px;
    color: #555;
    margin: 40px 0 20px 0;
    padding: 15px;
}

 .imgBox{
  margin: 10px 0px 10px 0px;
 }

 .typeWM{
  height: 100vh;
  background-color: #555;
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
  img{
    height: 450px;
  }

  .t1r{
  font-size: 1.5rem;
  color: #fff;
  margin: 50px 0 10px 0;
}

select{
    font-size: 15px;
    color: #555;
    margin: 20px 0 10px 0;
    padding: 10px;
}

 }

 @media only screen and (max-width: 1024px) {
  img{
      height: 400px;
    }
}

@media only screen and (max-width: 768px) {
   .typeWM{
  width: 100vw;
 }
   .cdown{
  width: 100vw;
 }
  img{
    height: 450px;
  }

  @media only screen and (max-width: 425px) {
    img{
    height: 400px;
  }
    .t2r{
  font-size: 30px;
  } 
 }
}

</style>