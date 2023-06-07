<template>
    <v-app :theme="dark">
      <NavBar></NavBar>
      <v-main
          class="main"
        >
            <OptionBar
              class="option"
              app
            >
            </OptionBar>    
            <router-view/>
         
      </v-main>
    </v-app>
</template>


<script setup>
import NavBar from './NavBar.vue';
import OptionBar from './OptionBar.vue';
//import SideBar from './SideBar.vue';
</script>

<style>

.main{
  z-index: 0 !important;
  position: relative !important;
}
.option{
  height: 85px !important;
}


</style>