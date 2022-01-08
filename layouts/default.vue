<template>
  <v-app dark>
    <v-app-bar
      style="opactiy:.5;"
      app
    >  
      <NuxtLink to="/">
        <nuxt-img 
          class="mx-2"
          src='/tdc-big.png'
          height="50"
        />
      </NuxtLink>
      <!-- <v-toolbar-title v-text="title" /> -->
      <v-spacer />
      <v-app-bar-items class="hidden-sm-and-down">
          <v-btn icon v-on:click="$vuetify.theme.dark = !$vuetify.theme.dark">
            <v-icon>mdi-white-balance-sunny</v-icon>
          </v-btn>
          <v-icon ></v-icon>
          <NuxtLink v-for="item in menuItems" v-bind:key="item.title" :to="item.link"><v-btn>{{item.title}}</v-btn></NuxtLink>
      </v-app-bar-items>

      <v-menu>
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
            class = "hidden-md-and-up"
          >
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </template>
        <v-list>
          <NuxtLink v-for="item in menuItems" v-bind:key="item.title" :to="item.link">
              <v-list-item>
                <v-list-item-title>
                  {{item.title}}
                </v-list-item-title>
              </v-list-item>
          </NuxtLink>
        </v-list>
      </v-menu>

    </v-app-bar>
    <v-main style="padding:0">
      <!-- <v-container> -->
        <Nuxt />
      <!-- </v-container> -->
    </v-main>
    <v-footer>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      title: 'TDC',
      menuItems: [
        {title: 'Home', link: '/'},
        {title: 'Members', link: '/members'},
        {title: 'Rush', link: '/rush'},
        // {title: 'History', link: '/history'},
        // {title: 'Photos', link: '/photos'},
      ]
    }
  }
}
</script>

