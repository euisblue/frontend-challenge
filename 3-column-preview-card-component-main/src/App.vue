<template>
  <div>
    <div id="content">
      <Panel icon="sedans" title="sedans" color="hsl(31, 77%, 52%)">
        <template  v-slot:description>  
          Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip.
        </template>
      </Panel>
      <Panel icon="suvs" title="suvs" color="hsl(184, 100%, 22%)">
        <template v-slot:description>
            Take an SUV for its spacious interior, power, a,nd versatility. Perfect for your next family vacation and off-road adventures.
        </template>
      </Panel>
      <Panel icon="luxury" title="luxury" color="hsl(179, 100%, 13%)">
        <template v-slot:description>
          Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style.
        </template>
      </Panel>
    </div>
    <Attribution name="imeubug"/>
  </div>
</template>

<script>
import Panel from './components/Panel'
import Attribution from './components/Attribution'

export default {
  name: 'App',
  components: {
    Attribution,
    Panel
  }
}
</script>

<style scoped>
#content {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin: 0 auto;
  border-radius: 10px;
  overflow: hidden;
}

</style>
