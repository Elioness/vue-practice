<template>
  <div>
    <h3>
        This is TodoPage component :D 
    </h3>

    <input type="text" placeholder="Add an item" v-model="item" />
    <button @click.prevent="addItem">Add</button>
    <ul>
        <li :v-for= " item in items "> {{ items }} </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TodoPage',

  data: function() {
    return {
      item: "",
      items: ["item1", "item2"]
    };
  },

  methods: {
    addItem: function () {
      this.items.push(this.item);
      this.item = "";
    }
  }
  
}
</script>

<style>

</style>