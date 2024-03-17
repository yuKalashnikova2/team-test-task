<script>
export default {
  props: {
    pagination: {
      type: Object,
      required: true,
    },
  },
  emit: ['setCurrentPage'],
}
</script>

<template>
  <div class="pagination">
    <button class="pagination__btn">
      <img src="/svg/prev.svg" alt="prev" />
    </button>

    <div v-for="i in pagination.totalPages" :key="i">
      <div
        v-if="
          i >= pagination.startFrom &&
          i < pagination.startFrom + pagination.showPagesFromStart
        "
      >
        <a
          class="pagination__item"
          :class="{
            pagination__item_active:
              i === pagination.currentPage ||
              (i === '1' && pagination.currentPage === 1),
          }"
          href=""
          @click.prevent="$emit('setCurrentPage', i)"
        >
          {{ i }}
        </a>
      </div>
    </div>

    <span
      class="pagination__item"
      @click="$emit('showPages', pagination.totalPages)"
      >...</span
    >
    <a
      :class="[
        'pagination__item',
        {
          pagination__item_active:
            pagination.totalPages == pagination.currentPage,
        },
      ]"
      @click.prevent="$emit('setCurrentPage', pagination.totalPages)"
      >{{ pagination.totalPages }}</a
    >
    <button class="pagination__btn">
      <img src="/svg/next.svg" alt="next" />
    </button>
  </div>
</template>

<style lang="scss" scoped>
.pagination {
  background-color: #fff;
  padding: 16px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  &__btn {
    background-color: #f5f5f5;
    border-radius: 6px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 20px;
    height: 20px;
    margin: 8px;
    cursor: pointer;
  }
  &__item {
    font-weight: 400;
    font-size: 14px;
    line-height: 143%;
    color: #8591ae;
    padding: 8px 14px;
    cursor: pointer;
    width: 36px;
    height: 36px;
    &_active {
      background-color: #f5f5f5;
      color: #2a355a;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 12px;
    }
  }
}
</style>
