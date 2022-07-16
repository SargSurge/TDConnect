<template>
  <div>
    <v-hover
      v-slot="{ hover }"
    >
      <v-card 
        :elevation="hover ? 16 : 2"
        :class="{ 'on-hover': hover }"
        style="margin:10px; padding:20px" 
        height="450"
        width="100%"
      >
        <v-row>
            <v-col>
                <nuxt-img height="325" width="275" :src="'/img' + event.img" />
            </v-col>
            <v-col>
                <h2>{{event.name}}</h2>
                <p>{{event.description}}</p>
            </v-col>
        </v-row>
      </v-card>
    </v-hover>
  </div>
</template>

<script>

export default {
  name: 'RushCard',
  props: ['event'],
  computed: {

  },
  data() {
      return {
      };
  },
}
</script>