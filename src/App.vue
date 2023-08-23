<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      elevate-on-scroll
      dark
    >
      <div class="d-flex align-center">
        <!-- lugar para colocar o nome -->
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

        <v-toolbar-title>Leandro Campolina</v-toolbar-title>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        text
      >
        <span class="mr-2">Home</span>
      </v-btn>
      <v-btn
        text
      >
        <span class="mr-2">About</span>
      </v-btn>
      <v-btn
        text
      >
        <span class="mr-2">Projects</span>
      </v-btn>
      <v-btn
        text
      >
        <span class="mr-2">Contact</span>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-btn
              text
            >
              <span class="mr-2">Home</span>
            </v-btn>
          </v-list-item>

          <v-list-item>
            <v-btn
              text
            >
              <span class="mr-2">About</span>
            </v-btn>
          </v-list-item>

          <v-list-item>
            <v-btn
              text
            >
              <span class="mr-2">Projects</span>
            </v-btn>
          </v-list-item>

          <v-list-item>
            <v-btn
              text
            >
              <span class="mr-2">Contact</span>
            </v-btn>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>
