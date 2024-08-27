<template>
  <div class="slider-filter">
    <h3>Цена</h3>
    <div class="slider-inputs">
      <div class="input-group">
        <span class="input-prefix">от</span>
        <input type="text" v-model="minPrice" />
      </div>
      <span class="divider">—</span>
      <div class="input-group">
        <span class="input-prefix">до</span>
        <input type="text" v-model="maxPrice" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      minPrice: '5 500 ₽',
      maxPrice: '5 500 ₽',
    };
  },
};
</script>

<style lang="scss">
@import '@/styles/variables.scss';

.slider-filter {
  h3 {
    text-align: center;
    vertical-align: middle;
    font-size: 16px;
    line-height: 20px;
    font-weight: 700;
    margin-bottom: 10px;
    color: $--color-font-main;
  }

  .slider-inputs {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;

    .input-group {
      position: relative;
      flex: 1;
      display: flex;
      align-items: center;
      border: 1px solid $--color-border;
      border-radius: 4px;
      padding: 5px;
    }

    .input-prefix {
      font-size: 12px;
      line-height: 14px;
      color: $--color-font-second;
      margin-right: 5px;
    }

    input[type="text"] {
      border: none;
      outline: none;
      width: 100%;
      flex: 1;
      font-size: 14px;
      color: $--color-font-main;
      padding: 5px;
      background-color: transparent;
    }

    .divider {
      color: $--color-font-second;
    }
  }
}
</style>
