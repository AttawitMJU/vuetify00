<script setup>
import { RouterLink, RouterView } from "vue-router";
// import HelloWorld from "./components/HelloWorld.vue";
// import { ref, watch } from "vue";

// const drawer = ref(false);
// const group = ref();
// const menu = ref([
//   {
//     title: "Foo",
//     value: "foo",
//   },
//   {
//     title: "Bar",
//     value: "bar",
//   },
//   {
//     title: "Fizz",
//     value: "fizz",
//   },
//   {
//     title: "Buzz",
//     value: "buzz",
//   },
// ]);

// watch(drawer.value, () => {
//   drawer.value = false;
// });
</script>

<template>
  <v-app>
    <v-app-bar
      title="Application"
      :elevation="1"
      color="primary"
      density="compact"
      ><template v-slot:prepend>
        <v-app-bar-nav-icon></v-app-bar-nav-icon> </template
    ></v-app-bar>
    <v-navigation-drawer expand-on-hover rail permanent location="right">
      <v-list>
        <v-list-item
          prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
          title="Sandra Adams"
          subtitle="sandra_a88@gmailcom"
        ></v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list density="compact" nav>
        <router-link to="/">
          <v-list-item
            prepend-icon="mdi-folder"
            title="My Files"
            value="myfiles"
          ></v-list-item
        ></router-link>
        <router-link to="/about"
          ><v-list-item
            prepend-icon="mdi-account-multiple"
            title="Shared with me"
            value="shared"
          ></v-list-item
        ></router-link>
        <v-list-item
          prepend-icon="mdi-star"
          title="Starred"
          value="starred"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container fluid> <router-view></router-view></v-container
    ></v-main>
  </v-app>
</template>
