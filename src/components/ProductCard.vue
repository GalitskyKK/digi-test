<template>
  <div class="product-card">
    <div class="image-wrapper">
      <div class="badge-wrapper">
        <span class="badge"
          >Хит продаж
          <img src="@/assets/fire-icon.svg" alt="Fire Icon" class="fire-icon" />
        </span>
      </div>
      <img src="@/assets/emptyItem.svg" alt="Product Image" />
      <span class="discount">25%</span>
    </div>
    <div class="details">
      <div class="brand">Бренд</div>
      <div class="product-name">
        {{ product.name }}
      </div>
      <div class="price-wrapper" v-if="product.isStock">
        <span class="price">{{ product.price }} ₽</span>
        <span class="old-price">{{ product.lastPrice }} ₽</span>
      </div>
      <button v-if="product.isStock" class="buy-button">Купить</button>
      <button v-if="!product.isStock" class="empty-button">Сообщить о поступлении</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

.product-card {
  width: 330px;
  border-radius: 4px;
  background-color: $--color-white;
  display: flex;
  flex-direction: column;
  gap: 16px;

  .badge-wrapper {
    position: absolute;
    top: 12px;
    left: 12px;
    display: flex;
    align-items: center;
    gap: 8px;

    .badge {
      background-color: $--color-font-bg;
      color: $--color-font-main;
      padding: 4px 8px;
      border-radius: 4px;
      font-size: 12px;
      display: flex;
      align-items: center;
    }

    .fire-icon {
      width: 20px;
      height: 20px;
    }
  }

  .image-wrapper {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f8f8f8;
    border-radius: 8px;
    padding: 16px;

    img {
      max-width: 330px;
    }

    .discount {
      position: absolute;
      bottom: 12px;
      left: 12px;
      background-color: $--color-brand;
      color: $--color-white;
      padding: 4px 8px;
      border-radius: 4px;
      font-size: 14px;
    }
  }

  .details {
    display: flex;
    flex-direction: column;
    align-items: start;
    .brand {
      color: $--color-font-second;
      font-size: 14px;
      margin-bottom: 8px;
    }

    .product-name {
      font-size: 14px;
      line-height: 18px;
      color: $--color-font-main;
      margin-bottom: 16px;
    }

    .price-wrapper {
      display: flex;
      align-items: center;
      gap: 8px;

      .price {
        color: $--color-font-main;
        font-size: 18px;
        font-weight: bold;
      }

      .old-price {
        color: $--color-font-second;
        font-size: 14px;
        text-decoration: line-through;
      }
    }

    .buy-button {
      padding: 10px;
      width: 75px;
      height: 38px;
      background-color: $--color-white;
      color: $--color-brand;
      border: 1px solid $--color-brand;
      border-radius: 4px;
      font-size: 14px;
      cursor: pointer;
      margin-top: 16px;
      font-weight: 600;
      transition: background-color 0.3s ease;

      &:hover {
        background-color: darken($--color-brand, 10%);
        color: $--color-white;
      }
    }

    .empty-button {
      width: 100%;
      height: 38px;
      color: $--color-font-second;
      background-color: #fff;
      border: 1px solid $--color-font-second;
      border-radius: 4px;
      font-size: 14px;
      cursor: pointer;
      margin-top: 39px;
      font-weight: 600;
      transition: background-color 0.3s ease;
      text-align: center;

      &:hover {
        background-color: darken($--color-font-second, 1%);;
        color: $--color-white;
      }
    }
  }
}

@media (max-width: 1440px) {
  .product-card {
    width: 210px;
  }

  .image-wrapper {
    img {
      width: 210px;
    }
  }
}

@media (max-width: 1024px) {
     .product-card {
    width: 160px;
  }

  .image-wrapper {
    img {
      width: 160px;
    }
  }
}

@media (max-width: 425px) {
     .product-card {
    width: 160px;
  }

  .image-wrapper {
    img {
      width: 160px;
    }
  }
}

@media (max-width: 375px) {
     .product-card {
    width: 160px;
  }

  .image-wrapper {
    img {
      width: 160px;
    }
  }
}

</style>
