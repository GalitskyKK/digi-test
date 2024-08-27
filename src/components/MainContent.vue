<template>
  <div class="main-content">
    <SearchBar />
    <div class="category-title">Название категории</div>
    <ProductList />
  </div>
</template>

<script>
import ProductList from './ProductList.vue';
import SearchBar from './SearchBar.vue';

export default {
  name: 'MainContent',
  components: {
    ProductList,
    SearchBar,
  },
};
</script>

<style lang="scss">
@import '@/styles/variables.scss';

.main-content {
  padding: 10px 0 36px 36px;
  flex: 1;

  h1 {
    font-size: 28px;
    margin-bottom: 20px;
    color: $--color-font-main;
  }

  .search-bar {
    display: none;
  }

  .category-title {
    display: none;
    padding: 12px;
    font-size: 24px;
    color: $--color-font-main;
  }

  @media (max-width: 425px) {
    .main-content {
      padding: 16px;
    }

    .search-bar {
      display: flex;
    }

    .category-title {
      display: block;
    }
  }

  @media (max-width: 375px) {
    .main-content {
      padding: 16px;
    }

    .search-bar {
      display: flex;
    }

    .category-title {
      display: block;
    }
  }
}

@media (max-width: 425px) {
  .main-content {
    padding: 16px;
  }
}

@media (max-width: 375px) {
  .main-content {
    padding: 16px;
  }
}
</style>
