<template>
  <div id="app">
    <h1>Vue Weather App</h1>
    <WeatherForm @weather-fetched="updateWeather" />
    <WeatherCard
      v-if="weather"
      :location="weather.location"
      :temperature="weather.temperature"
      :conditions="weather.conditions"
      :humidity="weather.humidity"
      :windSpeed="weather.windSpeed"
    />
  </div>
</template>

<script>
import WeatherForm from './components/WeatherForm.vue';
import WeatherCard from './components/WeatherCard.vue';

export default {
  components: {
    WeatherForm,
    WeatherCard
  },
  data() {
    return {
      weather: null
    };
  },
  methods: {
    updateWeather(data) {
      this.weather = data;
    }
  }
};
</script>
