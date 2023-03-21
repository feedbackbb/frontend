<template>
<div class="home container text-center">
  <div class="boxL">
    <inputC/><!-- เติมเงิน -->
  </div>

  <div class="boxR">
    <typeWM/><!-- เลือกประเภทเครื่องซักผ้า -->
  </div>

</div>
</template>

<script>
import inputC from "@/components/inputC.vue"
import typeWM from '@/components/typeWM.vue'
import countdown from '@/components/countdown.vue'

export default {
  name: "Home",
  components:{
    inputC,
    typeWM,
    countdown
  }
}
</script>

<style>
.home {
  display: flex;
  justify-content:space-between;
  width: 100vw;
  height: 100vh;
  align-items: center;
  
}
.boxL{
  /* width: 50vw; */
}
.boxR{
  /* width: 50vw; */
}
@media only screen and (max-width: 768px) {
  .home {
    display: flex;
    justify-content:space-between;
    width: 100vw;
    height: 100vh;
    align-items: center;
    flex-direction: column;
    
  }
}
</style>