<template>
  <div class="hello">
    <div class="fact" v-for="fact of facts" :key="fact">
      <span>{{ fact }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CatFacts',
  data() {
    return {
      facts: [],
    }
  },
  created() {
    fetch('https://meowfacts.herokuapp.com/?count=20')
      .then(response => response.json())
      .then(obj => {
        this.facts = obj.data;
      })
  },
}
</script>

<style scoped>
.hello {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.fact {
  margin: 1rem;
  padding: 1rem;
  background: rgb(228, 228, 228);
  color:black;
  border: 1px solid black;
  position:relative;
  display: flex;
  flex-direction: column;
  min-width: 200px;
  border-radius:6px;
}

</style>
