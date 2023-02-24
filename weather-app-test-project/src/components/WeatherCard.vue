<template>
  <q-card>
    <q-card-section class="card">
      <div class="locationWrapper">
        <span>Current Weather</span>
        <h5 class="location">{{ cityName ? cityName + ', ' + country : ''}}</h5>
      </div>
      <p>
        {{ temp ? 'Temperature: ' + Math.round(temp) + 'C&deg;' : ''}}
      </p>
      <p>
        {{ humidity ? 'Humidity: ' + Math.round(humidity) + '%' : ''}}
      </p>
      <p>
        {{ feelsLike ? 'Feels Like: ' + Math.round(feelsLike) + 'C&deg;' : ''}}
      </p>
      <div class="iconWrapper" v-if="weather == 'Snow'">
        {{weather}}<SnowIcon/>
      </div>
      <div class="iconWrapper" v-else-if="weather == 'Clouds'">
        {{weather}}<CloudIcon/>
      </div>
      <div class="iconWrapper" v-else-if="weather == 'Mist'">
        {{weather}}<MistIcon/>
      </div>
      <div class="iconWrapper" v-else-if="weather == 'Clear'">
        {{weather}}<ClearSkyIcon/>
      </div>
      <div class="iconWrapper" v-else-if="weather == 'Rain'">
        {{weather}}<RainIcon/>
      </div>
    </q-card-section>
  </q-card>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import  SnowIcon  from '../../public/snowIcon.vue'
import CloudIcon from '../../public/cloudIcon.vue'
import RainIcon from '../../public/rainIcon.vue'
import MistIcon from '../../public/mistIcon.vue'
import ClearSkyIcon from '../../public/clearSkyIcon.vue'

export default defineComponent ({
  name: 'WeatherCard',
  components: {
    SnowIcon,
    CloudIcon,
    ClearSkyIcon,
    MistIcon,
    RainIcon
  },
  props: {
    temp: Number,
    humidity: Number,
    feelsLike: Number,
    cityName: String,
    country: String,
    weather: String
  },
  setup() {
    
  }
})

</script>

<style scoped lang="scss">
.q-card {
  background-color: #E6E6E6;
  margin: 16px 50px;
  .card {
    height: 270px;
    width: 400px;
    .locationWrapper {
      .location {
        border-bottom: 1px solid gray;
        margin-bottom:  25px;
        margin-top: 10px;
      }
    }
   
    .iconWrapper {
      display: flex;
      align-items: center;
      svg {
        margin-left: 10px;
      }
    }
  }
}

</style>