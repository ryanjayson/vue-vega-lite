<template>
 <div class='dashboard'>
  <vega-lite :data="values" mark="bar" :encoding="encoding"></vega-lite>
 </div>
</template>

<script>
import Vue from 'vue';
import VueVega from 'vue-vega'

Vue.use(VueVega)

export default{
  data () {
    return {
      values: [
        {time: 'A', money: 28}, {time: 'B', money: 55}, {time: 'C', money: 43},
        {time: 'D', money: 91}, {time: 'E', money: 81}, {time: 'F', money: 53},
        {time: 'G', money: 19}, {time: 'H', money: 87}, {time: 'I', money: 52}
      ],
      encoding: {
        x: {field: 'time', type: 'ordinal'},
        y: {field: 'money', type: 'quantitative'}
      }
    }
  }
}
</script>
