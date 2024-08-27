<template>
  <div class="category-filter">
    <div class="category-filter__title">
      <h3>Название категории</h3>
      <span>3</span>
    </div>
    <ul>
      <li v-for="(category, index) in categories" :key="index" @click="toggleSubCategories(index)">
        <div class="category-item" :class="{ active: openCategory === index }">
          <span>{{ category.name }}</span>
          <span class="sub-categories">{{ category.subCategories.length }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      openCategory: null,
      categories: [
        {
          name: 'Категория 1',
          subCategories: ['Подкатегория 1', 'Подкатегория 2', 'Подкатегория 3'],
        },
        {
          name: 'Категория 2',
          subCategories: ['Подкатегория 1', 'Подкатегория 2', 'Подкатегория 3'],
        },
        {
          name: 'Категория 3',
          subCategories: ['Подкатегория 1', 'Подкатегория 2', 'Подкатегория 3'],
        },
      ],
    };
  },
  methods: {
    toggleSubCategories(index) {
      this.openCategory = this.openCategory === index ? null : index;
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';
.category-filter {
  &__title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: center;

    h3 {
      font-size: 14px;
      line-height: 16px;
      font-weight: 400;
      margin-bottom: 10px;
      color: $--color-font-main;
    }

    span {
      font-size: 14px;
      line-height: 16px;
      color: $--color-font-second;
    }
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;

    .category-item {
      font-size: 14px;
      line-height: 16px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      text-align: center;
      cursor: pointer;
      padding: 7px;
      padding-left: 32px;

      .sub-categories {
        font-size: 14px;
        line-height: 16px;
        color: $--color-font-second;
      }
    }

    .category-item.active {
      border-radius: 5px;
      background-color: $--color-font-bg;
    }
    .subcategories {
      padding-left: 15px;
      li {
        padding: 8px 0;
        font-size: 14px;
        line-height: 16px;
        color: $--color-font-second;
      }
    }
  }
}
</style>
