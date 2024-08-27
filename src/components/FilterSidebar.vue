<template>
  <div class="filter-sidebar">
    <CategoryFilter />
    <SliderFilter />
    <BrandCheckboxFilter />
    <SizeCheckboxFilter />
  </div>
</template>

<script>
import CategoryFilter from '@/components/filterSidebar/CategoryFilter.vue';
import SliderFilter from '@/components//filterSidebar/SliderFilter.vue';
import BrandCheckboxFilter from '@/components/filterSidebar/BrandCheckboxFilter.vue';
import SizeCheckboxFilter from '@/components/filterSidebar/SizeCheckboxFilter.vue';

export default {
  components: {
    CategoryFilter,
    SliderFilter,
    BrandCheckboxFilter,
    SizeCheckboxFilter,
  },
};
</script>

<style lang="scss">
@import '@/styles/variables.scss';

.filter-sidebar {
  display: flex;
  flex-direction: column;
  gap: 20px;
  width: 280px;
}
</style>
