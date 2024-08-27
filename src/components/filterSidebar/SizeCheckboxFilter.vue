<template>
  <div class="checkbox-filter">
    <h3>Размер</h3>
    <ul>
      <li v-for="(brand, index) in filteredBrands" :key="index">
        <label class="custom-checkbox">
          <input type="checkbox" v-model="selectedBrands" :value="brand" />
          {{ brand }}
        </label>
        <span>3</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: '',
      selectedBrands: [],
      brands: ['Атрибут', 'Атрибут1', 'Атрибут2', 'Атрибут3', 'Атрибут4', 'Атрибут5', 'Атрибут6'],
    };
  },
  computed: {
    filteredBrands() {
      return this.brands.filter((brand) => brand.toLowerCase().includes(this.search.toLowerCase()));
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

.checkbox-filter {
  h3 {
    text-align: center;
    vertical-align: middle;
    font-size: 16px;
    line-height: 20px;
    font-weight: 700;
    margin-bottom: 10px;
    color: $--color-font-main;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;

    li {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 12px;

      label {
        font-size: 14px;
        line-height: 16px;
        color: $--color-font-main;
        display: flex;
        align-items: center;
        cursor: pointer;

        input[type='checkbox'] {
          /* Увеличиваем размер чекбокса и добавляем фон */
          width: 20px;
          height: 20px;
          margin-right: 8px;
          border-radius: 3px;
          appearance: none; /* Убираем стандартный вид чекбокса */
          border: 1px solid $--color-border;
          position: relative;
          cursor: pointer;
        }

        input[type='checkbox']:checked {
          background-color: $--color-brand; /* Меняем цвет фона при выборе */
        }

        input[type='checkbox']::after {
          content: '';
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
          width: 14px;
          height: 14px;
          background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='%23fff'%3E%3Cpath d='M9 19L3 13l2-2 4 4 8-8 2 2z'/%3E%3C/svg%3E");
          background-size: cover;
        }
      }

      span {
        font-size: 14px;
        line-height: 16px;
        color: $--color-font-second;
      }
    }
  }
}
</style>
