<template>
  <div class="search-bar">
    <button class="back-btn">
      <img src="@/assets/ArrowLeft.svg" alt="Back" />
    </button>
    <input type="text" v-model="query" placeholder="Поиск" />
    <button class="clear-btn" @click="clearQuery">
      <img src="@/assets/SearchCrossDefault.svg" alt="Clear" />
    </button>
    <button class="search-btn">Найти</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      query: '',
    };
  },
  methods: {
    clearQuery() {
      this.query = '';
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

.search-bar {
   display: flex;
  align-items: center;
  border-bottom: 1px solid $--color-border;
  padding: 6px 0;
  gap: 6px;

  .back-btn {
    background: none;
    border: none;
    margin-right: 8px;
    cursor: pointer;

    img {
      width: 20px;
      height: 20px;
      max-width: 20px;
    }
  }

  input[type="text"] {
    border: none;
    outline: none;
    color: $--color-font-main;
    padding: 10px 0;
    font-size: 16px;
    padding-left: 10px;
    width: 100%;
  }

  .clear-btn {
    background: none;
    border: none;
    cursor: pointer;

    img {
      width: 20px;
      height: 20px;
      max-width: 20px;
    }
  }

  .search-btn {
    background-color: $--color-brand;
    color: $--color-white;
    border: none;
    padding: 12px 16px;
    border-radius: 4px;
    cursor: pointer;
  }
}

</style>