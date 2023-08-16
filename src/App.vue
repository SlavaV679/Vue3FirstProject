<template>
  <div>
    <ul>
      <li v-for="(item, idx) in items" :key="idx">
        {{ item.name }} - {{ item.price }}
      </li>
    </ul>
    <button @click="addAndUpdate">Add and update</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      items: [
        { name: "AlphVVV", price: 1 },
        { name: "BetaVVV", price: 2 },
      ],
    };
  },

  methods: {
    addAndUpdate() {
      const newItem = { name: "New", price: "-" };
      this.items.push(newItem);
      setTimeout(() => {
        newItem.price = "over 9000";
      }, 10);
    },
  },
};
</script>
