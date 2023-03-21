<template>
  <div class="countdown-container">
    <div class="countdown-number">{{ minutes }}</div>
    <div class="countdown-label">MINUTES</div>
    <div class="countdown-number">{{ seconds }}</div>
    <div class="countdown-label">SECONDS</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timeRemaining: 1800, // Set the initial time remaining in seconds
      minutes: 30, // Set the initial number of minutes
      seconds: 0, // Set the initial number of seconds
      timerId: null, // Will be used to reference the setInterval timer
    };
  },

  mounted() {
    // Start the countdown timer when the component is mounted
    this.timerId = setInterval(this.updateTime, 1000);
  },

  beforeDestroy() {
    // Stop the countdown timer when the component is destroyed
    clearInterval(this.timerId);
  },

  methods: {
    updateTime() {
      console.log(this.timeRemaining);
      if (this.timeRemaining > 0) {
        // If there is still time remaining, decrement the time remaining
        this.timeRemaining--;
        this.minutes = Math.floor(this.timeRemaining / 60);
        this.seconds = this.timeRemaining % 60;
      }  
      else {
        // If there is no time remaining, clear the interval timer
        clearInterval(this.timerId);
      }
      
      if(this.timeRemaining == 60){
        console.log("ทำความสะอาดจะเสร็จภายในอีก 1 นาที่");
      }
    },
  },
};
</script>

<style scoped>
.countdown-container {
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Arial, sans-serif;
  font-size: 3rem;
  font-weight: bold;
  color: #fff;
  background-color: #2c3e50;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
}

.countdown-label {
  font-size: 1rem;
  font-weight: normal;
  margin: 0 10px;
}

.countdown-number {
  display: inline-block;
  width: 50px;
  height: 50px;
  background-color: #1abc9c;
  border-radius: 50%;
  text-align: center;
  line-height: 50px;
  margin-right: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
</style>
