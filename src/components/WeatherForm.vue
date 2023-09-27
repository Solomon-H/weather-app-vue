<template>
  <div class="weather-form">
    <input v-model="location" placeholder="Enter location" />
    <button @click="getWeather">Get Weather</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      location: ''
    };
  },
  methods: {
    getWeather() {
      // Simulate an API call to fetch weather data
      this.$emit('weather-fetched', {
        location: this.location,
        temperature: Math.floor(Math.random() * 30) + 1,
        conditions: 'Sunny',
        humidity: Math.floor(Math.random() * 100) + 1,
        windSpeed: Math.floor(Math.random() * 20) + 1
      });
    }
  }
};
</script>

<style scoped>
.weather-form {
  margin: 20px;
}
</style>
