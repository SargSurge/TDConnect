<template>
  <v-row>
    <v-col class="text-center">
      <h1>Members of TDC</h1>
      <MemberList style="margin-top:30px" v-bind:members="members2023" />
    </v-col>
  </v-row>
</template>

<script>
import MemberList from '../components/MemberList.vue';

export default {
  name: 'MembersPage',
  components: [MemberList],
  data () {
    return {
      members2023: [
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