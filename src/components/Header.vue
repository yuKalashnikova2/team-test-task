<template>
  <div class="header">
    <div class="header__name">
      <img src="/svg/header.svg" alt="burger" />
      <h1 class="header__name__title">Team</h1>
    </div>

    <div class="header__info">
      <div class="header__info__icons">
        <img src="/svg/search.svg" alt="search" />
        <img src="/svg/bell.svg" alt="bell" />
        <div class="header__divider"></div>
      </div>
  
      <div class="header__info__user">
        <div class="header__info__user__avatar">
          <img src="/avatar.png" alt="avatar" />
        </div>

        <p>Ernest Eberly</p>
        <div class="header__info__user__arrow">
          <img src="/svg/path.svg" alt="arrow" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 22px 28px;
  background: linear-gradient(to right,#f3f9ff, #fff);;
  &__name {
    display: flex;
    gap: 28px;
    &__title {
      font-weight: 500;
      font-size: 22px;
      line-height: 150%;
      color: #2a355a;
    }
  }
  &__info {
    display: flex;
    &__icons {
      display: flex;
      padding: 3px 4px;
      & > * {
        margin-right: 28px;
      }
    }
    &__user {
      display: flex;
      align-items: center;
      gap: 12px;
      &__avatar {
        border-radius: 8px;
        overflow: hidden;
        flex-shrink: 0;
        width: 32px;
        height: 32px;
        & img {
          width: 100%;
        }
      }
      & p {
        font-weight: 500;
        font-size: 14px;
        line-height: 143%;
        color: #2a355a;
      }
      &__arrow {
        background-color: #f5f7fb;
        border-radius: 6px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 20px;
        height: 20px;
        & img {
          padding: 8px 6px;
        }
      }
    }
  }
  &__divider {
    background-color: #e5e8ef;
    border: 1px solid #e5e8ef;
  }
}
</style>
