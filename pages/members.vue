<template>
  <v-container style="padding-top:100px">
    <v-row>
      <v-col class="text-center">
        <h1>Members of TDC</h1>
        <v-btn
          v-for="year in ['All', 2025, 2024, 2023, 2022, 2021]"
          v-bind:key="year"
          v-on:click="selectedYear = year"
          style="margin:10px;"
          color="navy"
          elevation="1"
          outlined
          tile
          x-large
          :disabled="selectedYear == year"
        >{{year}}</v-btn>
        <MemberList style="margin-top:30px" v-bind:members="selectedMembers" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import MemberList from '../components/MemberList.vue';

export default {
  name: 'MembersPage',
  components: {MemberList},
  computed: {
    selectedMembers() {
      return this.members.filter(m => (m.year == this.selectedYear) || this.selectedYear == 'All');
    }
  },
  data () {
    return {
      selectedYear: 'All',
      members: [
          {
            name: 'Sergio Perez',
            hometown: 'Lakeland, FL',
            course: '6-3',
            bio: 'Snorlax in real life.',
            img: '/sergio.jpeg',
            year: '2023'
          },
          {
            name: 'Sergio Perez',
            hometown: 'Lakeland, FL',
            course: '6-3',
            bio: 'Snorlax in real life.',
            img: '/sergio.jpeg',
            year: '2023'
          },
          {
            name: 'Sergio Perez',
            hometown: 'Lakeland, FL',
            course: '6-3',
            bio: 'Snorlax in real life.',
            img: '/sergio.jpeg',
            year: '2023'
          },
          {
            name: 'Sergio Perez',
            hometown: 'Lakeland, FL',
            course: '6-3',
            bio: 'Snorlax in real life.',
            img: '/sergio.jpeg',
            year: '2023'
          },
        ],
    };
  },
  
}
</script>