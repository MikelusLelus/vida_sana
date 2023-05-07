<template>
  <div>
    <div :class="[pausat ? 'tempo' : 'tempo-on']">{{ formatTime }}</div>
    <button class="boto-tempo" @click="pausat ? startTimer() : restartTimer()">{{ pausat ? 'Començar' : 'Reiniciar' }}</button>
    <audio ref="audio"></audio>
  </div>
</template>

<script>
export default {
  name: "Temporitzador",
  props: {
    minuts: {
      type: Number,
      required: true,
    },
    audioSrc: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      temps: 0,
      interval: null,
      pausat: true,
    };
  },
  created() {
    this.temps = this.minuts * 60 * 1000;
  },
  methods: {
    startTimer() {
      this.$refs.audio.src = this.audioSrc;
      this.$refs.audio.play();
      this.pausat = false;
      if (this.interval) {
        clearInterval(this.interval);
      }
      this.interval = setInterval(() => {
        if (this.temps > 0) {
          this.temps -= 1000;
        } else {
          clearInterval(this.interval);
        }
      }, 1000);
    },
    restartTimer() {
      this.$refs.audio.currentTime = 0;
      this.$refs.audio.pause();
      clearInterval(this.interval);
      this.temps = this.minuts * 60 * 1000;
      this.pausat = true;
    },
  },
  computed: {
    formatTime() {
      const minutes = Math.floor(this.temps / 60000);
      const seconds = Math.floor((this.temps % 60000) / 1000);
      return `${minutes.toString().padStart(2, "0")}:${seconds
        .toString()
        .padStart(2, "0")}`;
    },
  },
};
</script>

<style scoped>
.tempo{
    font-family: 'Roboto', sans-serif;
    font-weight: 400;
    font-size: 9rem;
    border-radius: 50%;
    background-color: white;
    color: #1565C0;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 500px;
    height: 500px;
  }
.tempo-on {
    font-family: 'Roboto', sans-serif;
    font-weight: 400;
    font-size: 9rem;
    border-radius: 50%;
    background-color: #1565C0;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 500px;
    height: 500px;
}
.boto-tempo {
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  font-size: 18px;
  background-color: white;
  color: #1565C0;
  padding: 10px 35px;
  border: 1px solid black;
  border-radius: 20px;
  margin-top: 30px;
  cursor: pointer;
}

.boto-tempo:hover {
  background-color: #1565C0;
  color: white;
}
</style>
  