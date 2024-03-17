<script>
import Button from './Button.vue'
export default {
  components: {
    Button,
  },
  props: {
    avatar: {
      type: String,
      default: 'profile',
    },
    name: {
      type: String,
      default: 'Name',
    },
    team: {
      type: String,
      default: 'Team',
    },
    role: {
      type: String,
      default: 'Role',
    },
    email: {
      type: String,
      default: 'Email',
    },
    birthday: {
      type: String,
      default: 'Birthday',
    },
    telegram: {
      type: String,
      default: 'Telegram',
    },
    lostLogin: {
      type: String,
      default: 'Lost Login',
    },
  },
}
</script>
<template>
  <div class="table__item">
    <div class="table__item__user">
      <div
        :class="[
          'table__item__avatar',
          avatar === 'women.svg' ? 'table__item__avatar_bg-women' : '',
          avatar === 'men.svg' ? 'table__item__avatar_bg-men' : ''
        ]"
      >
        <img
          :src="'/svg/table-employee/avatars/' + avatar"
          :alt="avatar"
        />
        <img
          v-if="avatar === ''"
          src="/svg/table-employee/avatars/profile.svg"
          alt="profile"
        />
      </div>
      <span>{{ name }}</span>
    </div>

    <span>{{ team }}</span>
    <span>{{ role }}</span>
    <span>{{ email }}</span>
    <span>{{ birthday }}</span>
    <span>{{ telegram }}</span>
    <span>{{ lostLogin }}</span>

    <div class="table__item__buttons">
      <Button label="Edit" transparent>
        <img src="/svg/table-employee/edit.svg" alt="edit" />
      </Button>

      <div>
        <img src="/svg/table-employee/trash-delete.svg" alt="trash" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.table__item {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  align-items: center;
  font-weight: 400;
  font-size: 14px;
  line-height: 143%;
  width: 100%;
  color: #2a355a;

  & > * {
    padding: 22px 16px;
  }
  & span {
    display: block;
  }
  &__user {
    display: flex;
    gap: 12px;
    align-items: center;
  }
  &__avatar {
    border-radius: 12px;
    width: 36px;
    height: 36px;
    overflow: hidden;
    flex-shrink: 0;
    & img {
      width: 100%;
    }
    &_bg-women {
      background-color: #feadad;
      padding: 4px;
    }
    &_bg-men {
      background-color: #8ECAFE;
      padding: 4px;
    }
  }
  &__buttons {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 50px;
  }
}
</style>
