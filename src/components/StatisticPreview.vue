<script>
export default {
  props: {
    statisticList: {
      type: Array,
      required: true,
    },
  },
}
</script>

<template>
  <div class="statistic">
    <div class="statistic__title">
      <div class="statistic__title__icon">
        <svg
          width="20"
          height="21"
          viewBox="0 0 20 21"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M11.4732 9.65182C12.2868 10.4654 12.2868 11.7845 11.4732 12.5981C10.6596 13.4117 9.34049 13.4117 8.5269 12.5981C7.7133 11.7845 7.7133 10.4654 8.5269 9.65182C9.34049 8.83823 10.6596 8.83823 11.4732 9.65182"
            stroke="#1E96FC"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M16.0448 4.65185C16.8584 5.46544 16.8584 6.78453 16.0448 7.59813C15.2312 8.41172 13.9122 8.41172 13.0986 7.59813C12.285 6.78453 12.285 5.46544 13.0986 4.65185C13.9122 3.83826 15.2312 3.83826 16.0448 4.65185"
            stroke="#1E96FC"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M15 10.7083C16.2775 10.7083 17.5 11.1525 18.3333 11.8192"
            stroke="#1E96FC"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M6.90149 4.65185C7.71508 5.46544 7.71508 6.78453 6.90149 7.59813C6.08789 8.41172 4.7688 8.41172 3.95521 7.59813C3.14162 6.78453 3.14162 5.46544 3.95521 4.65185C4.7688 3.83826 6.08789 3.83826 6.90149 4.65185"
            stroke="#1E96FC"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M1.66667 11.8192C2.50001 11.1525 3.72251 10.7083 5.00001 10.7083"
            stroke="#1E96FC"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M13.8258 16.9583C12.855 16.2075 11.46 15.7083 10 15.7083C8.54001 15.7083 7.14501 16.2075 6.17418 16.9583"
            stroke="#1E96FC"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </div>
      <div class="statistic__title__text">
        <h2>Team</h2>
        <div class="statistic__title__text__icon">
          <img src="/svg/i.svg" alt="" />
        </div>
      </div>
    </div>

    <div class="statistic__content">
      <ul class="statistic__content__list">
        <li
          v-for="item in statisticList"
          class="statistic__content__list__item"
        >
          <span
            >{{ item.quantity }}
            <div v-if="item.title == 'online'" class="online-green"></div>
          </span>
          <p>{{ item.title }}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.statistic {
  background-color: #fff;
  padding: 16px 28px;
  border-radius: 12px;
  display: flex;
  gap: 50px;
  @media (max-width: 767px) {
    flex-direction: column;
  }
  &__title {
    display: flex;
    align-items: center;
    gap: 16px;
    &__icon {
      background-color: #f3f9ff;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 8px;
      width: 32px;
      height: 32px;
    }
    &__text {
      position: relative;
      & h2 {
        font-weight: 500;
        font-size: 14px;
        line-height: 143%;
        color: #2a355a;
      }

      &__icon {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #f5f5f5;
        border-radius: 50%;
        width: 14px;
        height: 14px;
        position: absolute;
        top: 0;
        right: -16px;
      }
    }
  }
  &__content {
    &__list {
      display: flex;
      @media (max-width: 767px) {
        flex-direction: column;
      }
      & li:not(:last-child) {
        border-right: 1px solid #e5e8ef;
      }

      &__item {
        display: flex;
        flex-direction: column;
        padding-right: 36px;
        padding-left: 36px;
        position: relative;
        & span {
          display: block;
          font-weight: 500;
          font-size: 22px;
          line-height: 130%;
          color: #2a355a;
        }
        & p {
          display: block;
          font-weight: 400;
          font-size: 12px;
          line-height: 150%;
          color: #8591ae;
        }
      }
    }
  }
}

.online-green {
  background-color: #24c182;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  position: absolute;
  right: 32px;
  top: 6px;
}
</style>
