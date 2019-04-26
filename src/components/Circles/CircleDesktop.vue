<template>
  <vue-circle
      v-if="activateAnimation"
      :progress="progressValue"
      :size="400"
      :reverse="false"
      line-cap="round"
      :fill="fill"
      empty-fill="rgba(251, 251, 251, 0)"
      :animation-start-value="0.0"
      :animation="isDuration"
      :start-angle="0"
      insert-mode="append"
      :thickness="3"
      ref="circle"
      @vue-circle-progress="resolveProgress">
  </vue-circle>
</template>

<script>
import VueCircle from 'vue2-circle-progress'

export default {
name: "CircleDesktop",
props: ['activateAnimation', 'progressValue', 'isDuration', 'fill', 'currentProgress'],
components: {
VueCircle,
},
methods: {
resolveProgress(event, progress, stepValue) {
this.$emit('progress', event, progress, stepValue)
}
},
watch: {
'currentProgress'(value) {
if (value === 75) {
setTimeout(() => {
console.log()
this.$refs.circle.updateProgress(0)
}, 2000)
}
if (value === 0) {
setTimeout(() => {
this.$refs.circle.updateProgress(75)
}, 2000)
}
}
}
}
</script>

<style scoped>

</style>
