<template>
  <div class="search-input">
    <input type="text" v-model="query" placeholder="Поиск по товарам по 100 000 товаров" />
  </div>
</template>

<script>
export default {
  name: 'SearchInput',
  data() {
    return {
      query: ''
    };
  },
  methods: {
    search() {
      console.log(`Поиск по запросу: ${this.query}`);
    }
  }
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

.search-input {
  display: flex;
  align-items: center;

  input {
    padding: 11px;
    border: 1px solid $--color-brand;
    border-radius: 10px;
    font-size: 16px;
    line-height: 24px;
    font-weight: 400;
    flex: 1;
    padding-left: 48px;
    background-image: url(../assets/search-icon.svg);
    background-repeat: no-repeat;
    background-position: 10px center;
    background-size: 24px;
  }

  button {
    padding: 10px 20px;
    background-color: $--color-brand;
    color: $--color-white;
    border: none;
    border-radius: 5px;
    cursor: pointer;

    &:hover {
      background-color: darken($--color-brand, 10%);
    }
  }
}
</style>
