<template>
  <div id="app">
    <h1>{{ title }}</h1>

    <h4>No config : up up down down left right left right b a</h4>
    <easteregg>EASTER EGG</easteregg>

    <h4>Change title: easter or up down</h4>
    <easteregg @easter="test" :eggs="eggs"></easteregg>

    <h4>Visibility duration: duration</h4>
    <easteregg :duration="5000" :eggs="dureggs">5 seconds</easteregg>
  </div>
</template>

<script>
import easteregg from '../src/easteregg.vue'

export default {
  name: 'app',
  data () {
    return {
      title: 'vue-easteregg',
      eggs: [ 
        'easter',
        [ 'ArrowUp', 'ArrowDown' ]
      ],
      dureggs: [ 
        'duration'
      ]
    }
  },
  components: { easteregg },
  methods: {
    test () {
      if (this.title === 'vue-easteregg') {
        this.title = 'EASTER EGGGG !!!!'
      } else if (this.title === 'EASTER EGGGG !!!!') {
        this.title = 'AGAIN ??'
      } else {
        this.title = 'vue-easteregg'
      }
    }
  }
}
</script>

<style>

</style>
