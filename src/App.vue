<script>
import Header from './components/Header.vue'
import SideBar from './components/SideBar.vue'
import StatisticPreview from './components/StatisticPreview.vue'
import Button from './components/Button.vue'
import TableEmployee from './components/TableEmployee.vue'
import Pagination from './components/Pagination.vue'

export default {
  components: {
    Header,
    SideBar,
    StatisticPreview,
    Button,
    TableEmployee,
    Pagination,
  },
  data() {
    return {
      pagination: {
        currentPage: 1,
        totalPages: 12,
        showPagesFromStart: 3,
        startFrom: 1,
        showDots: true,
      },
      sidebarImages: [
        'tools',
        'city',
        'money',
        'link',
        'planner',
        'circle',
        'settings',
        'business',
        'team',
      ],
      statisticList: [
        { quantity: 130, title: 'members' },
        { quantity: 36, title: 'online' },
        { quantity: 50, title: 'men' },
        { quantity: 80, title: 'women' },
        { quantity: 29, title: 'average age' },
        { quantity: 265, title: 'days work on average' },
        { quantity: 36, title: 'days work newest employee' },
        { quantity: 1256, title: 'days work oldest employee' },
      ],
      employees: [
        {
          avatar: 'sarah.png',
          name: 'Sarah Connor',
          team: 'Crosty',
          role: 'Team Lead',
          email: 'sarahconnor@gmail.com',
          birthday: '25.04.1994',
          telegram: '@sarahconnor',
          lostLogin: '03.11.2021',
        },
        {
          avatar: 'women.svg',
          name: 'Arnold Brown',
          team: 'Gunters',
          role: 'Seo Specialist',
          email: 'arnoldbrown@gmail.com',
          birthday: '12.04.1989',
          telegram: '@arnoldbrown',
          lostLogin: '02.11.2021',
        },
        {
          avatar: 'ernest.png',
          name: 'Ernest Eberly',
          team: 'Flamethrower',
          role: 'Semantic Specialist',
          email: 'ernesteberly@gmail.com',
          birthday: '17.06.1993',
          telegram: '@ErnestEberly',
          lostLogin: '03.11.2021',
        },
        {
          avatar: 'lance.png',
          name: 'Lance Thomas',
          team: 'Wizards',
          role: 'Seo Specialist',
          email: 'lancethomas@gmail.com',
          birthday: '12.04.1989',
          telegram: '@LanceThomas',
          lostLogin: '02.11.2021',
        },
        {
          avatar: 'cheryl.png',
          name: 'Cheryl Glover',
          team: 'Gunters',
          role: 'Python Programmist',
          email: 'cherylglover@gmail.com',
          birthday: '15.08.1985',
          telegram: '@CherylGlover',
          lostLogin: '03.11.2021',
        },
        {
          avatar: 'men.svg',
          name: 'Lance Thomas',
          team: 'Crosty',
          role: 'Seo Specialist',
          email: 'lancethomas@gmail.com',
          birthday: '12.04.1989',
          telegram: '@LanceThomas',
          lostLogin: '01.11.2021',
        },
        {
          avatar: 'ernest.png',
          name: 'Ernest Eberly',
          team: 'Flamethrower',
          role: 'Semantic Specialist',
          email: 'ernesteberly@gmail.com',
          birthday: '17.06.1993',
          telegram: '@ErnestEberly',
          lostLogin: '03.11.2021',
        },
        {
          avatar: 'lance.png',
          name: 'Lance Thomas',
          team: 'Wizards',
          role: 'Seo Specialist',
          email: 'lancethomas@gmail.com',
          birthday: '12.04.1989',
          telegram: '@LanceThomas',
          lostLogin: '02.11.2021',
        },
        {
          avatar: 'cheryl.png',
          name: 'Cheryl Glover',
          team: 'Gunters',
          role: 'Python Programmist',
          email: 'cherylglover@gmail.com',
          birthday: '15.08.1985',
          telegram: '@CherylGlover',
          lostLogin: '03.11.2021',
        },
      ],
    }
  },
  methods: {
    setCurrentPage(page) {
      console.log(page)
      this.pagination.currentPage = page
    },
  },
}
</script>

<template>
  <div class="container">
    <div class="wrapper">
      <div>
        <SideBar :sidebarImages="sidebarImages" />
      </div>
      <div>
        <Header />
        <div class="bg">
          <StatisticPreview :statisticList="statisticList" />
          <Button label="Add new Employee">
            <img src="/svg/btn-plus.svg" alt="plus" />
          </Button>
          <TableEmployee :employees="employees" />

          <Pagination
            :pagination="pagination"
            @setCurrentPage="setCurrentPage($event)"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: scroll;
}
.wrapper {
  width: 100%;
  border-radius: 12px 12px 12px 12px;
  margin: auto;
  background-color: #fff;
  margin: auto;
  display: flex;
}
.bg {
  background-color: #f3f9ff;
  padding: 28px;
  & > * {
    margin-bottom: 28px;
  }
}
</style>
