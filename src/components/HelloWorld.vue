<template>
  <div class="hello">
    <input type="text" v-model="filter">

<ul>
    <li v-for="items in filteredItems">{{ items.name }}</li>
</ul>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      filter: '',
      item: [
        {name: 'Koos', age: 30, eyes: 'red'},
        {name: 'Gert', age: 20, eyes: 'blue'},
        {name: 'Pieter', age: 12, eyes: 'green'},
        {name: 'Dawid', age: 67, eyes: 'dark green'},
        {name: 'Johan', age: 15, eyes: 'purple'},
        {name: 'Hans', age: 12, eyes: 'pink'},
        {name: 'GGG', age: 12, eyes: 'pink'}
      ]
    }
  },
  methods: {
  },
  computed: {
    filteredItems () {
      return this.item.filter((item) => {
        return item.name.indexOf(this.filter) > -1
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
