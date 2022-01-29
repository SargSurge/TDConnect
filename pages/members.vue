<template>
  <v-container style="padding-top:100px; padding-bottom:50px">
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
      return this.currentMembers.filter(m => (m.year == this.selectedYear) || this.selectedYear == 'All').sort(this.sortMembers);
    }
  },
  methods: {
    sortMembers (a, b) {
      if (a.name < b.name && a.year <= b.year) {return -1;}
      if (a.name > b.name && a.year >= b.year) {return 1;}
      return 0;
    }
  },
  data () {
    return {
      selectedYear: 'All',
      currentMembers: [
        {
            name: 'Sergio Perez',
            hometown: 'Lakeland, FL',
            course: '6-3',
            bio: 'Sergio “Surge” Perez is a rising sophomore studying Computer Science with a minor in Economics. He attributes his success as MIT Robotics Team’s Chief Marketing Officer to his experience playing Rocket League. Sergio says that being brother of TDC has helped him grow as an individual and explore what he is truly passionate about. This summer he is working on his Course 15 UROP, working on an optimization algorithm for flight scheduling. He is already set on gaining his Masters of Engineering, specializing in artificial intelligence.',
            img: '/surge.png',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2023'
          },
          {
            name: 'Rafael Olivera-Cintron',
            hometown: 'Orlando, FL',
            course: '6-2 & 2',
            bio: 'Rafael Olivera-Cintrón is a Puerto Rican from Orlando, Florida majoring in 6-2 with a minor in 4B and 2. Rafael’s inclination towards populism and problem-solving, enables his interests in policy, entrepreneurship, and innovation. Currently, Rafael spends time outside of school working with his UROP and the MIT Hyperloop Team. He is also on the Campus Activities Complex Institute Committee, is the TDC Recruitment Chair, Alumni Relations Chair, and Undergraduate Representative on the Strategy Working Team. After graduating, Rafael wants to start a company for innovation that promotes business ethics, and the fair treatment of workers, and also optimizes costs to make technology accessible to all people. He also wants to help create a political, social system that meets the needs of all people and does not take advantage of the resources of underprivileged communities.',
            img: '/rafa.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2022'
          },
          {
            name: 'Fernando Rendon',
            hometown: 'McAllen, TX',
            course: '2A-15',
            bio: 'Fernando “Ferny” Rendon hails from the south border, splitting his citizenship between the US and Mexico. Because he enjoys breaking things apart and solving problems, Ferny declared mechanical engineering as his major. Aside from class, Ferny HAs the Sloan “Intro to Making” class as well as works with high school students through MIT OEOP’s SEED program. He breaks stereotypical Mexcian machismo energy as a member of MIT’s Cheerleading team. Ferny has spent the year working at PCC Aerostructures-Progressive as an engineering co-op improving the manufacturing process of F-35 bulkheads.',
            img: '/ferny.jpeg',
            song: 'https://open.spotify.com/track/4TCeFZNjGNQIpCuZmJkkE2?si=dfa6a27351084a68',
            year: '2021'
          },
          {
            name: 'Emerson Vaquerano',
            hometown: 'Chelsea, MA',
            course: '6-3',
            bio: 'Emerson Vaquerano is the snake charmer of the house, being the father of his snake “Aisnley.” He is majoring in computer science for two reasons: the money and just cause he enjoys coding. Emerson can usually be found on the first floor playing a few tunes or so on the house piano. Emerson worked as TA for MIT OEOP’s SEED program teaching programming to high school students. This summer Emerson is taking time for himself and searching for an internship.',
            img: '/emerson.jpeg',
            song: 'https://open.spotify.com/track/1sFstGV1Z3Aw5TDFCiT7vK?si=95ad9e6c4de147f4',
            year: '2021'
          },
          {
            name: 'Terry Kang',
            hometown: 'Reddit',
            course: '18C',
            bio: 'Terry Kang is a rising junior studying mathematics. He appreciates the existence and the observation of the aquatic bird of the Spheniscidae family, more commonly known as the humble penguin. Alongside the gratitude he holds for Aptenodytes, he has a keen interest in media that pertains in the objective of cognitive arousal within a sexual context. It is an understood assumption that since his arrival into consciousness, the general public and the world at large has reverted some level of positive progress previously made.',
            img: '/terry.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2022'
          },
          {
            name: 'Ben Barrera',
            hometown: 'Houston, TX',
            course: '6-9',
            bio: 'Ben Barrera is a Course 6-9 (Computation and Cognition) major from Houston, Texas. Infamous for steering casual conversations in a neuroscientific direction, it’s no surprise that he has been thinking about the mind and brain since a young age. In his free time, he wanders between different genres of music, playing the tuba and bass trombone with concert and jazz ensembles, and producing music for growing Houston-based rap and r&b artists. He has hopes of starting a record label over the next year. Having grown up, in part, in a small town in central Mexico, Ben used to wake up every day to the horizon-filling sight of a volcano with ash plumes spewing from its summit.',
            img: '/ben.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2022'
          },
          {
            name: 'Mohit Dighamber',
            hometown: 'Ohio',
            course: '8',
            bio: "I am also a sophomore majoring in physics and minoring in mathematics. Outside of TDC, I spend my time UROPing in astrophysics, leading MIT's QuestBridge chapter, and playing the piano. Fun fact about me: I have moved a total of ten times in my life.",
            img: '/mohit.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2023'
          },
          {
            name: 'Sebastian Portalatin',
            hometown: 'San Juan, PR',
            course: '6-3',
            bio: "Sebastián Portalatín is a rising sophomore currently studying Course 18-C (Math and Computer Science). The math part is his true love, and the computer science part pays the bills. This summer, Sebastián interned at a Puerto Rican startup called Sociants, developing [REDACTED] to help connect people in need to non-profits who can help them. No cap, Sebastián's dream is to open a restaurant. Outside of school, Sebastián loves learning languages, getting swole, and re-creating board games online.",
            img: '/polta.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2023'
          },
          {
            name: 'Nicolas Suter',
            hometown: 'Glendale, CA',
            course: '18C & 21M-Music',
            bio: "Nicolas Suter is a '23 double majoring in 18C and 21M-Music. He loves listening to progressive metal, alt hip hop, and jazz fusion. He likes to eat good food, spend time with his friends, and remind his fellow TDCs to drink water.\nAcademically, he's interested in theoretical computer science, especially in algorithms, and he is pursuing a career in quantitative finance.",
            img: '/nicolas.jpeg',
            song: 'https://open.spotify.com/track/7hBygJQ4O8ZPKTLtkNxrve?si=ed4ffc84e8b743c6',
            year: '2023'
          },
          {
            name: 'Trinity Stallins',
            hometown: 'Arlington, TX',
            course: '11 & 2A-1',
            bio: 'TBD',
            img: '/trinity.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2023'
          },
          {
            name: 'Justice Vidal',
            hometown: 'Elmont, NY',
            course: '6-2',
            bio: 'TBD',
            img: '/justice.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2023'
          },
          {
            name: 'Otilia Don',
            hometown: 'Chisinau, Moldova',
            course: '9',
            bio: 'TBD',
            img: '/otilia.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2022'
          },
          {
            name: 'Rodrigo Posada',
            hometown: 'San Ignacio, El Salvador',
            course: '18',
            bio: 'TBD',
            img: '/rodrigo.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2022'
          },
          {
            name: 'Edgardo Letona',
            hometown: 'San Salvador, El Salvador',
            course: '14',
            bio: 'TBD',
            img: '/edgardo.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2022'
          },
          {
            name: 'Ygor Moura',
            hometown: 'Niterói, Rio de Janeiro, Brasil',
            course: '5 & 6-3',
            bio: 'Straight out of a fake hemisphere, ygor will try one of those things with you:\n1) feed you\n2) hug you\n3) compliment you\n4) explain what computational chemistry is\nIn any of these cases do not trust him as he has been reported for illegal activity for the Russian government. Suspicious activity include: majoring in chemistry, interest in computer science, sleeping and waking up early-ish, swimming, cooking, participation in the International Student Association, involvement in Banana Lounge activities (known for making social experiments), love for the beach and warm weather. Under request will give you an comprehensive playlist for Brazilian music, do not ask about sad cats as it can cause serious emotional damage to the subject',
            img: '/ygor.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2024'
          },
          {
            name: 'Pip Engeriser',
            hometown: 'Mobile, AL',
            course: '6-3',
            bio: 'TBD',
            img: '/pip.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2024'
          },
          {
            name: 'Andrii Zahorodnii',
            hometown: 'Kyiv, Ukraine',
            course: '18C',
            bio: 'TBD',
            img: '/andrii.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2024'
          },
          {
            name: 'Joaquin Dubon',
            hometown: 'San Salvador, El Salvador',
            course: '8',
            bio: 'TBD',
            img: '/joaquin.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2024'
          },
          {
            name: 'Vlada Petrusenko',
            hometown: 'Kyiv, Ukraine',
            course: '6-3',
            bio: 'TBD',
            img: '/sergio.jpeg',
            song: 'https://open.spotify.com/track/10Nmj3JCNoMeBQ87uw5j8k?si=05f793a6b01d44d1',
            year: '2024'
          },
          {
            name: 'Skye Borrero',
            hometown: 'Orlando, FL',
            course: '16',
            bio: 'TBD',
            img: '/skye.png',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2024'
          },
          {
            name: 'Samuel Lima',
            hometown: 'Fortaleza, Brasil',
            course: '6-2',
            bio: 'TBD',
            img: '/sam.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2024'
          },
          {
            name: 'David Turturean',
            hometown: 'Suceava, Romania',
            course: 'life',
            bio: 'TBD',
            img: '/david.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2025'
          },
          {
            name: 'Ionel Chiosa',
            hometown: 'Onesti, Romania',
            course: '6',
            bio: 'TBD',
            img: '/ionel.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2025'
          },
          {
            name: 'Jaime Punyed',
            hometown: 'San Salvador, El Salvador',
            course: '6',
            bio: 'TBD',
            img: '/sergio.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2025'
          },
          {
            name: 'Sabrina Queipo',
            hometown: 'Maracaibo, Venezuela',
            course: '6',
            bio: 'TBD',
            img: '/sabrina.jpeg',
            song: 'https://open.spotify.com/track/7lPN2DXiMsVn7XUKtOW1CS?si=a970908e401149c0',
            year: '2025'
          }
        ]
    };
  },
  
}
</script>