<template>
  <div>
    <h1>{{ message }}</h1> <!-- Text Interpolation -->
    <p v-html="rawHTML"></p> <!-- Raw HTML -->
    <div :id="dynamicId">{{ dynamicText }}</div> <!-- Attribute Bindings -->
    <p>{{ 2 + 2 }}</p> <!-- JavaScript expressions inside syntax -->

    <button @click="sayHello">Click me</button> <!-- Event Handling -->

    <p>Reactive Counter: {{ counter }}</p> <!-- Reactivity Fundamentals -->
    <button @click="incrementCounter">Increment</button>

    <p>Computed Property: {{ computedValue }}</p> <!-- Computed Properties -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello, Vue 3!',
      rawHTML: '<span style="color: red;">Red Text</span>',
      dynamicId: 'elementId',
      dynamicText: 'Dynamic Text',
      counter: 0,
    };
  },
  computed: {
    computedValue() {
      return this.counter * 2;
    },
  },
  methods: {
    sayHello() {
      alert('Hello from Vue 3!');
    },
    incrementCounter() {
      this.counter++;
    },
  },
};
</script>

<style scoped>
/* CSS specific to this component */
</style>
