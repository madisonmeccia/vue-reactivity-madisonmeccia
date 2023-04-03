<script>
export default {
  // reactive state
  data() {
    return {
      count: 0,
      items: ["item 1", "item 2", "item 3"],
    };
  },

  // functions that mutate state and trigger updates
  methods: {
    increment() {
      this.count++;
    },
    addItem() {
      items.push("item 4");
    },
  },

  // lifecycle hooks
  mounted() {
    console.log(`The initial count is ${this.count}.`);
  },
};
</script>

<template>
  <button @click="addItem">Count is: {{ count }}</button>
  <ul>
    <li v-for="item in items">{{ item }}</li>
  </ul>
</template>
