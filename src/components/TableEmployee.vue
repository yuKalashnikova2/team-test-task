<script>
import TableEmployeeHeader from './TableEmployeeHeader.vue'
import TableEmloyeeItem from './TableEmloyeeItem.vue'
export default {
  components: {
    TableEmployeeHeader,
    TableEmloyeeItem,
  },
  props: {
    employees: {
      type: Array,
      required: false,
    },
  },
}
</script>
<template>
  <div class="table">
    <TableEmployeeHeader />
    <div>
      <TableEmloyeeItem
        v-for="(emp, i) in employees"
        :key="i"
        :avatar="emp.avatar"
        :name="emp.name"
        :team="emp.team"
        :role="emp.role"
        :email="emp.email"
        :birthday="emp.birthday"
        :telegram="emp.telegram"
        :lostLogin="emp.lostLogin"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.table {
  background: #fff;
  border-radius: 12px;
  padding: 16px;
}
</style>
