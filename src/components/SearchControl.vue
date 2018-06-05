<template>
  <div class="parent-div">
    <div class="search">
      <h1>Pok&eacutemon Search</h1>
      <form @submit.prevent="onSearch(search)">
        <label>Search by name: </label>
        <input v-model="search" placeholder="pikachu">
        </form>
    </div>
    <div class="button">
      <button type="submit">Search</button>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      search: ''
    };
  },
  props: {
    onSearch: {
      type: Function,
      required: true
    }
  }
};
</script>

<style>
button{
  margin-left: 10px;
}

.search {
  position: absolute;
  top: 35%;
  left: 60%;
  object-fit: contain;
  width: 320px;
}

.button {
  position: absolute;
  top: 79%;
  left: 58%;
}

button {
  padding: 10px;
  width: 150px;
  border-radius: 10px;
  border: 3px solid black;
  font-size: 2em;
  cursor: pointer;
}

</style>
