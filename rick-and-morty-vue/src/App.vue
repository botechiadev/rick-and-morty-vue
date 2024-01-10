<template>
  <header>
      <h1>Rick and Morty</h1>
      <FilterByStatus/>
      <FilterByName/>
    </header>
  <ListCharacters/>
</template>

<script>
import ListCharacters from './components/ListCharacters.vue';
import FilterByStatus from './components/FilterByStatus.vue';
import FilterByName from './components/FilterByName.vue';
export default {
  name: 'App',
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName
}
}
</script>

<style lang="scss">
*{
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

  :root{
    --background-card: #3c3e44;
    --background-body: #24282f;
    --text-orange: #ff9800;
    --text-gray: #c0c0c0;
    --text-white: #FFFFFF;
font-family: 'Montserrat', sans-serif;
  }


  body{
    display: grid;
    max-width: 1fr;
    min-height: 100vh;
    background-color: var(--background-body);
    color: var(--text-white);
  }

  h1{
    margin-bottom: 3rem;
    text-align: center;
    color: var(--background-body);
  }
  header{
    background-color: var(--text-white);
    padding: 4rem;
  }
</style>
