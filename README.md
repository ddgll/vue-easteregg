# VUE3 Version: https://github.com/ddgll/vue3-easteregg


# vue-easteregg

ADD an easter egg to your vue app ;)

``` javascript
<template>
  <div id="app">
    {{ title }}
    <easteregg @easter="test" :eggs="eggs" duration="5000">EASTER EGG</easteregg>
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
```
