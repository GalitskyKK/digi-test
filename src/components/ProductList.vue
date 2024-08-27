<template>
  <div class="product-list">
    <ProductCard v-for="product in products" :key="product.id" :product="product" />
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue';

export default {
  name: 'ProductList',
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 2,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 3,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: false,
        },
        {
          id: 4,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 5,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 6,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 7,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 9,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 10,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 11,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 12,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 13,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 14,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 15,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
        {
          id: 16,
          name: 'Полное название товара в несколько строк для вида с обрывом в конце...',
          price: 1999,
          lastPrice: 2999,
          isStock: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import '@/styles/variables.scss';

.product-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(330px, 1fr));
  gap: 24px;
}

@media (max-width: 1440px) {
  .product-list {
    grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
    gap: 24px;
  }
}

@media (max-width: 375px) {
  .product-list {
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 12px;
  }
}
</style>
