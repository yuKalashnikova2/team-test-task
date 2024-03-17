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
    }
}
//   data() {
//     return {
//       employees: [
//         {
//           avatar: 'sarah.png',
//           name: 'Sarah Connor',
//           team: 'Crosty',
//           role: 'Team Lead',
//           email: 'sarahconnor@gmail.com',
//           birthday: '25.04.1994',
//           telegram: '@sarahconnor',
//           lostLogin: '03.11.2021',
//         },
//         {
//           avatar: 'women.svg',
//           name: 'Arnold Brown',
//           team: 'Gunters',
//           role: 'Seo Specialist',
//           email: 'arnoldbrown@gmail.com',
//           birthday: '12.04.1989',
//           telegram: '@arnoldbrown',
//           lostLogin: '02.11.2021',
//         },
//         {
//           avatar: 'ernest.png',
//           name: 'Ernest Eberly',
//           team: 'Flamethrower',
//           role: 'Semantic Specialist',
//           email: 'ernesteberly@gmail.com',
//           birthday: '17.06.1993',
//           telegram: '@ErnestEberly',
//           lostLogin: '03.11.2021',
//         },
//         {
//           avatar: 'lance.png',
//           name: 'Lance Thomas',
//           team: 'Wizards',
//           role: 'Seo Specialist',
//           email: 'lancethomas@gmail.com',
//           birthday: '12.04.1989',
//           telegram: '@LanceThomas',
//           lostLogin: '02.11.2021',
//         },
//         {
//           avatar: 'cheryl.png',
//           name: 'Cheryl Glover',
//           team: 'Gunters',
//           role: 'Python Programmist',
//           email: 'cherylglover@gmail.com',
//           birthday: '15.08.1985',
//           telegram: '@CherylGlover',
//           lostLogin: '03.11.2021',
//         },
//         {
//           avatar: 'men.svg',
//           name: 'Lance Thomas',
//           team: 'Crosty',
//           role: 'Seo Specialist',
//           email: 'lancethomas@gmail.com',
//           birthday: '12.04.1989',
//           telegram: '@LanceThomas',
//           lostLogin: '01.11.2021',
//         },
//         {
//           avatar: 'ernest.png',
//           name: 'Ernest Eberly',
//           team: 'Flamethrower',
//           role: 'Semantic Specialist',
//           email: 'ernesteberly@gmail.com',
//           birthday: '17.06.1993',
//           telegram: '@ErnestEberly',
//           lostLogin: '03.11.2021',
//         },
//         {
//           avatar: 'lance.png',
//           name: 'Lance Thomas',
//           team: 'Wizards',
//           role: 'Seo Specialist',
//           email: 'lancethomas@gmail.com',
//           birthday: '12.04.1989',
//           telegram: '@LanceThomas',
//           lostLogin: '02.11.2021',
//         },
//         {
//           avatar: 'cheryl.png',
//           name: 'Cheryl Glover',
//           team: 'Gunters',
//           role: 'Python Programmist',
//           email: 'cherylglover@gmail.com',
//           birthday: '15.08.1985',
//           telegram: '@CherylGlover',
//           lostLogin: '03.11.2021',
//         },
//       ],
//     }
//   },
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
