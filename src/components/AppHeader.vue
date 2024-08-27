<template>
  <header class="header">
    <div class="header__logo">
      <img src="@/assets/logo.svg" alt="Логотип" />
    </div>
    <div class="header__catalog">
      <button>Каталог</button>
    </div>
    <div class="header__search">
      <SearchInput />
    </div>
    <nav class="header__nav">
      <a href="#">Информация о компании</a>
      <a href="#">Контакты</a>
      <a href="#">Полезные ссылки</a>
    </nav>
  </header>
</template>

<script>
import SearchInput from './SearchInput.vue';

export default {
  name: 'AppHeader',
  components: {
    SearchInput,
  },
};
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';

.header {
  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: center;
  gap: 24px;
  padding: 12px 0;

  &__logo {
    img {
      max-width: 145px;
      height: 48px;
    }
  }

  &__catalog {
    button {
      padding: 15.5px 24px;
      border-radius: 8px;
      border: 1px solid $--color-brand;
      background-color: $--color-white;
      cursor: pointer;
      font-weight: 600;
    }
  }

  &__nav {
    display: flex;
    gap: 20px;

    a {
      color: $--color-font-main;
      font-size: 14px;

      &:hover {
        color: $--color-font-hover;
      }
    }
  }

  &__search {
    max-width: 1015px;
    width: 100%;
    input {
      padding: 10px;
      border: 1px solid $--color-border;
      border-radius: 5px;
    }
  }
}

@media (max-width: 1440px) {
  .header__search {
    max-width: 479px;
  }
}

</style>
