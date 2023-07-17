<template>
  <v-app>
    <v-main class="body">
      <UserInfo/>
      <!-- <CenterPet class="fill-height align-center" justify-center/>  -->
      <ThePet/>
      <BottomLine/>
    </v-main>
  </v-app>
</template>

<script>
  import UserInfo from './components/UserInfo.vue'
  import ThePet from './components/ThePet.vue'
  import BottomLine from './components/BottomLine.vue'
  // import CenterPet from './components/CenterPet.vue'
  export default {
    name: 'App',

    components: {
      UserInfo,
      ThePet,
      BottomLine,
      // CenterPet
    }

  }
</script>

<style scoped>
  .body{
    background-color: antiquewhite;
  }
</style>
