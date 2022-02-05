<template>
    <div class="inputCircle"
      v-for='input in inputs'
      :key="input.id"
      :input = "input" 
      >
 
        <input
          type="text" 
          v-model="input.variableValue"
          :min="this.minHeight"
          :max="this.maxHeight"
          @input="resettingTheValue($event)"
        />
        <input
          class="styled-slider"
          type="range"
          :min="this.minHeight"
          :max="this.maxHeight"
          v-model="input.variableValue"
        />

    </div>
</template>

<script>
export default {
  name: 'MyCircle',
  // props: ['changeValue'],
  props: {changeValue: "inputs.customValue"},
  
  data() {
    return {
      minHeight: 0,
      maxHeight: 1000,
    }
  },
}
</script>
<style scoped>
</style>
