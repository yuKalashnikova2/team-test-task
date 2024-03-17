<template>
  <div class="table__header">
    <div class="table__header__item">
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/search.svg" alt="" />
      </div>

      <p>Business Name</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/open-arrow.svg" alt="" />
      </div>
    </div>
    <div class="table__header__item">
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/closed.svg" alt="" />
      </div>

      <p>Team</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/arrow-active.svg" alt="" />
      </div>
      <div class="table__header__item__icon table__header__item__icon_bg">
        <img src="/svg/table-employee/path.svg" alt="" />
      </div>
    </div>
    <div class="table__header__item">
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/closed.svg" alt="" />
      </div>

      <p>Role</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/open-arrow.svg" alt="" />
      </div>
      <div class="table__header__item__icon table__header__item__icon_bg">
        <img src="/svg/table-employee/path.svg" alt="" />
      </div>
    </div>

    <div class="table__header__item">
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/search.svg" alt="" />
      </div>

      <p>Gmail</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/open-arrow.svg" alt="" />
      </div>
    </div>

    <div class="table__header__item">
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/closed.svg" alt="" />
      </div>

      <p>Birthday</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/open-arrow.svg" alt="" />
      </div>
      <div class="table__header__item__icon table__header__item__icon_bg">
        <img src="/svg/table-employee/path.svg" alt="" />
      </div>
    </div>

    <div class="table__header__item">
      <p>Telegram</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/open-arrow.svg" alt="" />
      </div>
    </div>
    <div class="table__header__item">
      <p>Last Login</p>
      <div class="table__header__item__icon">
        <img src="/svg/table-employee/open-arrow.svg" alt="" />
      </div>
    </div>

    <div class="table__header__item">
      <p>User Permissions</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.table__header {
  display: flex;
  background: #f5f5f5;
  border-radius: 12px;

  &__item {
    display: flex;
    align-items: center;
    gap: 4px;
    padding: 16px 22px;
    &:not(:last-child) {
      border-right: 1px solid #e5e8ef;
    }
    & p {
      font-weight: 500;
      font-size: 12px;
      line-height: 130%;
      color: #2a355a;
    }
    &__icon {
      width: 20px;
      height: 20px;
      cursor: pointer;
      &_bg {
        background-color: #fff;
        border-radius: 6px;
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
  }
}
</style>
