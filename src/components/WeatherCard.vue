<template>
  <div class="weather-card">
    <h2>{{ location }}</h2>
    <p>Temperature: {{ temperature }}°C</p>
    <p>Conditions: {{ conditions }}</p>
    <p>Humidity: {{ humidity }}%</p>
    <p>Wind Speed: {{ windSpeed }} km/h</p>
  </div>
</template>

<script>
export default {
  props: {
    location: String
  },
  data() {
    return {
      temperature: 25,
      conditions: 'Sunny',
      humidity: 50,
      windSpeed: 10
    };
  }
};
</script>

<style scoped>
.weather-card {
  border: 1px solid #ccc;
  padding: 20px;
  margin: 10px;
}
</style>
