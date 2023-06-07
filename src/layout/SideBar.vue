<template>
    <v-navigation-drawer
    >
        <v-list-item
            lines="two"
            prepend-avatar="https://randomuser.me/api/portraits/women/81.jpg"
            title="Jane Smith"
            subtitle="Em sessão"
            
          ></v-list-item>
        
          <v-divider></v-divider>

          <v-list  nav>
            <v-list-item prepend-icon="mdi-home-city" title="Home" value="home"></v-list-item>
            <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
            <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users"></v-list-item>
          </v-list>
    </v-navigation-drawer>
</template>

<script setup>


</script>