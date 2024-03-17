<script>
export default {
    props: {
      sidebarImages: {
        type: Array,
        required: true,
      }
    }
//   data() {
//     return {
//       images: [
//         'tools',
//         'city',
//         'money',
//         'link',
//         'planner',
//         'circle',
//         'settings',
//         'business',
//         'team',
//       ],
//     }
//   },
}
</script>

<template>
  <div class="sidebar">
    <div class="sidebar__top">
      <div class="sidebar__top__logo">
        <img src="/svg/logo.svg" alt="logo" />
      </div>

      <div class="sidebar__top__menu">
        <div
          class="sidebar__top__menu__item"
          v-for="image in sidebarImages"
          :key="image"
        >
          <div
            v-if="image == 'team'"
            class="sidebar__top__menu__item__circle"
          ></div>
          <img :src="'/svg/sidebar/' + image + '.svg'" :alt="image" />
        </div>
      </div>
    </div>
    <div class="sidebar__main"></div>
    <div class="sidebar__footer">
      <div class="sidebar__footer__plus">
            <img src="/svg/plus.svg" alt="plus" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  max-width: 72px;
 height: 100%;
  &__top {
    padding-top: 28px;
    padding-bottom: 28px;
    display: flex;
    flex-direction: column;



    &__logo {
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 28px 26px;
    }
    &__menu {
      display: flex;
      flex-direction: column;
      gap: 8px;
      &__item {
        padding: 12px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        position: relative;
        &:hover {
          background-color: #e5e8ef;
        }
        &__circle {
          width: 4px;
          height: 20px;
          background-color: #8f20ef;
          transform: rotate(-180deg);
          border-radius: 100px 0 0 100px;
          position: absolute;
          left: 0;
        }
      }
    }
  }
&__main {
    flex-grow: 1;
    // flex-shrink: 0;
    // height: 100%;
}
  &__footer {
    flex-shrink: 0;
    margin-top: auto;
    border-top: 1px solid #e5e8ef;
    padding: 28px;
    &__plus {
      background-color: #f5f7fb;
      width: 20px;
      height: 20px;
      border-radius: 6px;
      cursor: pointer;
    }
  }
}
</style>
