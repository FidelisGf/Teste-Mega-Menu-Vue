<template>
    <v-container>
        <v-row 
            class="flex-column" 
            color="red"
        >
        <v-sheet 
            :height="55"
            :width="'100%'" 
            color="grey-darken-2"
            elevation="2"
            style="z-index: 2"
            class="
                d-flex 
                align-center 
                justify-center
            "
        >
            <v-row class="justify-start align-center">
                <v-col cols="2">
                    <v-btn
                        class="dropbtn"
                        variant="text"
                        @mouseover="show = true"
                        @mouseleave="show = false"        
                    >
                        <v-icon>
                            mdi-menu
                        </v-icon>
                        <p class="ml-2">Categorias</p>
                    </v-btn>
                </v-col>
               
            </v-row>
        </v-sheet>
        <transition name="fade">
            <v-container class="
            mt-n4 linha2 
            d-flex justify-center " 
              v-if="show"
              @mouseover="show = true"
              @mouseleave="show = false"
              style="z-index: 1"
              fluid
            >
                <v-card
                    class="linha"
                    dense
                    width="98%"
                >
                    <v-row
                        width="100%"
                    >
                        <v-col 
                            v-for="(item, index) in itens"
                            :key="index"
                            :value="index"
                            class="itens align-start justify-start"
                            :cols="'3'"
                        >
                            <v-list
                            >
                                <v-list-item class="align-start text-justify" >
                                    <v-col
                                        class="
                                        mt-n3 
                                        text-body-2
                                        text-xl-subtitle-1 
                                        font-italic 
                                        font-weight-bold 
                                        "
                                    >
                                        {{ item.label }}
                                    </v-col>
                                    <v-col
                                        class="mt-n3 "
                                        v-for="(categoria, index) in item.cat"
                                        :key="index"
                                    >
                                        <a 
                                            class="
                                            links 
                                            text-caption
                                            text-xl-body-2 
                                            font-weight-medium
                                            " 
                                            href="#" v-if="index < 3"
                                        >
                                            {{categoria.name}}
                                        </a>
                                        <a 
                                            class="
                                                links 
                                                text-caption
                                                text-xl-body-2 
                                                font-weight-black
                                            " 
                                            v-else 
                                            href="#"
                                        >
                                            Ver mais
                                            <v-icon size="small">
                                                mdi-arrow-down
                                            </v-icon>
                                        </a>
                                    </v-col>
                                </v-list-item>
                            </v-list>
                        </v-col>
                    </v-row>
                </v-card>
            </v-container>
        </transition>
    </v-row>

    </v-container>
   
</template>

<script setup>
import {ref} from 'vue'
const itens = 
ref([
                    {
                          id: 1,
                          label: 'Veiculos',
                          cat : [
                            {
                              id: 1,
                              name: 'Carros'    
                            },
                            {
                              id: 2,
                              name: 'Motos'    
                            },
                            {
                              id: 3,
                              name: 'Maquinas'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }

                          ]
                    },
                    {
                          id: 2,
                          label: 'Camping',
                          cat : [
                            {
                              id: 1,
                              name: 'Fogueiras'    
                            },
                            {
                              id: 2,
                              name: 'Cadeiras'    
                            },
                            {
                              id: 3,
                              name: 'Barracas'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    },
                    {
                          id: 3,
                          label: 'Banheiros',
                          cat : [
                            {
                              id: 1,
                              name: 'Chuveiros'    
                            },
                            {
                              id: 2,
                              name: 'Sanitários'    
                            },
                            {
                              id: 3,
                              name: 'Lixeiros'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    },
                    {
                          id: 4,
                          label: 'Jardim',
                          cat : [
                            {
                              id: 1,
                              name: 'Sementes'    
                            },
                            {
                              id: 2,
                              name: 'Enxadas'    
                            },
                            {
                              id: 3,
                              name: 'Mesas'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    },  
                    {
                          id: 5,
                          label: 'Churrasco',
                          cat : [
                            {
                              id: 1,
                              name: 'Churrasqueiras'    
                            },
                            {
                              id: 2,
                              name: 'Carvões'    
                            },
                            {
                              id: 3,
                              name: 'Tabua de corte'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    },
                    {
                          id: 6,
                          label: 'Casa & Lazer',
                          cat : [
                            {
                              id: 1,
                              name: 'Sofás'    
                            },
                            {
                              id: 2,
                              name: 'Televisões'    
                            },
                            {
                              id: 3,
                              name: 'Bancadas'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    },
                    {
                          id: 7,
                          label: 'Eletrônicos & Gaming',
                          cat : [
                            {
                              id: 1,
                              name: 'Caixas de som'    
                            },
                            {
                              id: 2,
                              name: 'Placas de video'    
                            },
                            {
                              id: 3,
                              name: 'Processadores'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    },
                    {
                          id: 8,
                          label: 'Cozinha & Derivados',
                          cat : [
                            {
                              id: 1,
                              name: 'Fogões'    
                            },
                            {
                              id: 2,
                              name: 'Armários'    
                            },
                            {
                              id: 3,
                              name: 'Geladeiras'    
                            },
                            {
                              id: 4,
                              name: 'Outros'    
                            }
                          ]
                    }

])


const show = ref(false)

</script>

<style setup>
.red{
    background-color: red !important;
    
}
.dropdown:hover .dropdown-content {
    display: block !important;
}
.dropdown-content{
    display: none !important;
}
.fade-enter-active, .fade-leave-active {
    transition: opacity 0.9s !important;
  }
.fade-enter, .fade-leave-to /* .fade-leave-active em versões anteriores a 2.1.8 */ {
    opacity: 0 !important;
}
.fade-enter-active{
    transition: 0.9s;
}
.linha{
    position: absolute !important;
    z-index: 0 !important;
}
.linha2{
    position: relative  !important;
}
.links{
    text-decoration: none !important;
    color: rgb(27, 27, 27) !important;
}

</style>