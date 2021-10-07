<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <v-card
    class="mx-auto"
    height="300"
    width="300"
    >
    <v-navigation-drawer
      absolute
      dark
      src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
      width="100%"
      permanent
    >
    <v-list>
        <v-list-item
          v-for="([icon, text], i) in items"
          :key="i"
          link
        >
        <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
        </v-list-item-content>
        </v-list-item>
    </v-list>
    </v-navigation-drawer>
    </v-card>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
        drawer: null,
        items: [
        ['mdi-email', 'Inbox'],
        ['mdi-account-supervisor-circle', 'Supervisors'],
        ['mdi-clock-start', 'Clock-in'],
        ]
        }),
  }
</script>
