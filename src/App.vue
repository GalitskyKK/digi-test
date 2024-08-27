<template>
  <div id="app">
    <Header id="header" />
    <div class="app-content">
      <FilterSidebar id="filter-sidebar" />
      <MainContent />
    </div>
  </div>
</template>

<script>
import Header from './components/AppHeader.vue';
import FilterSidebar from './components/FilterSidebar.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  components: {
    Header,
    FilterSidebar,
    MainContent,
  },
};
</script>

<style lang="scss">
@import '@/styles/main.scss';

#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
  padding: 0 100px;
  max-width: 1720px;

  .app-content {
    display: flex;
    flex: 1;
  }
}

@media (max-width: 425px) {

  #app {
    padding: 0;
  }

  #header {
    display: none;
  }

  #filter-sidebar {
    display: none;
  }
}

@media (max-width: 375px) {

  #app {
    padding: 0;
  }

  #header {
    display: none;
  }

  #filter-sidebar {
    display: none;
  }
}

</style>
