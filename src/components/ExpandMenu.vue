<template>
  <v-menu 
    offset-y
    open-on-hover :close-on-content-click="false"
    :location="'bottom'"
  >
  <template v-slot:activator="{ props }">
      <v-btn
        v-bind="props"
      >
        {{nmBtn}}
        <v-icon class="ml-1">
            mdi-arrow-down
        </v-icon>
      </v-btn>
  </template>
  <v-card
    scrollable
    :theme="theme"
    :color="base_color"
    class="menus-cat"
  > 
    <v-card-title> 
        {{titulo}}
    </v-card-title>
    <v-row
        :color="base_color"
    >
      <v-col 
        v-for="(item, index) in dados"
        :key="index"
        :value="index"
        class="itens"
        :cols="colunas"
      >
        <v-list
            :style="'background-color :' + base_color"
        >
          <v-list-item >
            <v-col
                class="mt-n3"
            >
                {{ item.label }}
            </v-col>
            <v-col
                class="mt-n3"
                v-for="(categoria, index) in item.cat"
                :key="index"
            >
                {{categoria.name}}
            </v-col>
          </v-list-item>
      </v-list>
      </v-col>
    </v-row>
  </v-card>
</v-menu>
</template>

<script>
    export default{
        data(){
            return{
               
            }
        },
        props : {
            titulo : String,
            nmBtn : String,
            colunas : String,
            dados : Object,
            base_color : String,
            theme : String,
            attch : String
        }   
    }

</script>
<style>
    .menus-cat{
        max-height: 550px !important;
        max-width: 80% !important;
    }

</style>

