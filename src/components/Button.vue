<script>
export default {
  props: {
    label: {
      type: String,
      default: 'Button',
    },
    transparent: {
      type: Boolean,
      required: false,
    },
  },
}
</script>

<template>
  <button :class="['button', transparent ? 'button_transparent' : '']">
    <div class="button__icon">
      <slot />
    </div>

    <span class="button__text">{{ label }}</span>
  </button>
</template>

<style lang="scss" scoped>
.button {
  display: flex;
  gap: 12px;
  border-radius: 12px;
  padding: 14px 16px;
  background-color: #8f20ef;
  color: #fff;
  cursor: pointer;
  &:hover {
    opacity: 0.9;
  }
  &__icon {
    width: 20px;
    height: 20px;
  }
  &__text {
    font-weight: 400;
    font-size: 14px;
    line-height: 143%;
  }
  &_transparent {
    background-color: #fff;
    border: 1px solid #e5e8ef;
    border-radius: 8px;
    color: #2a355a;
    gap: 8px;
    padding: 6px 12px;
  }
}
</style>
