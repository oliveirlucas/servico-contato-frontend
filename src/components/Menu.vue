<template>
  <v-container>
    <v-row>
      <v-col cols="6">
        <v-dialog
        transition="dialog-top-transition"
        scrollable
        max-width="600"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
            color="blue-grey darken-1"
            class="ma-2 white--text"
            fab
            tile
            text
            v-bind="attrs"
            v-on="on"
            width="150px"
            height="150px"
          >
            <div>
              <v-row>
                  <v-img
                    width="15px"
                    src="../assets/bussola.png"
                  ></v-img>
              </v-row>
              <br>
              <v-row>
                <span class="mt-2 text-capitalize"> Como utilizar </span>
              </v-row>
            </div>
          </v-btn>
          </template>
          <template v-slot:default="dialog">
            <v-card>
              <v-toolbar
                color="primary"
                dark
              >Como utilizar</v-toolbar>
              <v-divider></v-divider>
              <v-card-text>
                <div class="text-subtitle-2 pa-1">
                <span>
                <b>• Como o app pode te ajudar</b><br><br>

                Esse aplicativo foi feito para que você tenha em suas mãos as respostas para aquelas perguntas insistentes que surgem sempre que você sai de casa: <i>“Será que fechei a porta?”, “Será que fechei as janelas?”, “Apaguei as luzes?”</i>
                Através do <b>check list</b> você poderá listar todas essas tarefas e verifica-las antes de sair de casa, fazendo com que seu trajeto até o trabalho ou encontro com os amigos seja mais tranquilo. Sempre que as dúvidas surgirem, você pode dar uma olhadinha aqui e confirmar a conclusão das tarefas. 
                Além disso, você tem a função <b>Meu diário</b> que permite incluir um emoji referente ao seu humor do dia e principalmente fazer anotações naqueles dias difíceis identificando o que causou tamanha ansiedade. 
                A função <b>Me acalmar</b> deixa a disposição uma playlist de músicas calmas, técnicas de relaxamento e meditação guiada, para usar quando sentir necessidade.
                Você ainda terá acesso a informações a respeito do transtorno obsessivo-compulsivo por meio do ícone <b>Dúvidas</b> e também poderá acompanhar junto da sua (seu) psicóloga (o) a evolução do seu tratamento através do <b>Tempo de uso</b> do app.
                
                <br><br><b>• Ei, leia aqui, é importante </b><br><br>

                É importante saber que este aplicativo não tem o objetivo de tratar o transtorno, já que o tratamento é individual e deverá ser acompanhado por um profissional de psicologia. O que buscamos com este app é diminuir os impactos que os comportamentos repetitivos e indesejáveis podem causar a vida do sujeito. 
                Sendo assim, com ele você poderá passar mais tempo com seus amigos e familiares sem realizar as verificações de costume confiando nas informações do check list. Essa técnica é importante e eficaz, pois de acordo com os estudos as relações interpessoais e as habilidades sociais são fortes aliadas no tratamento do TOC. 
                
                <br><br><b>• Anote tudo</b><br><br>

                Existem estudos que indicam os benefícios de manter um diário. No nosso caso, as anotações sobre os eventos que te causam ansiedade são importantes para que possamos traçar estratégias de enfrentamento quando as situações acontecerem. Mas fique tranquilo! A identificação desses estímulos e o planejamento das estratégias deverão ser feitas com a ajuda de um profissional de psicologia e de acordo com os seus limites. 
                
                <br><br><b>• Construindo novos hábitos</b><br><br>

                Sabemos que o TOC não é uma coisa fácil! Além dos pensamentos intrusivos e os comportamentos indesejáveis, ele pode acabar te afastando de pessoas e lugares que você gosta. Portanto, com a ajuda do app aposte nesses relacionamentos: saia com os amigos, visite novos lugares, conheça pessoas novas, pois tudo isso poderá fazer diferença no seu tratamento. 
              
                </span>
                </div>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                  text
                  @click="dialog.value = false"
                >Fechar</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
      <v-col cols="6">
        <v-dialog
        transition="dialog-top-transition"
        scrollable
        max-width="600"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="blue-grey darken-1"
              class="ma-2 white--text"
              fab
              tile
              text
              v-bind="attrs"
              v-on="on"
              width="150px"
              height="150px"
            >
              <div>
                <v-row>
                    <v-img
                      src="../assets/Duvida.png"
                    ></v-img>
                </v-row>
                <br>
                <v-row class="justify-center">
                  <span class="mt-3 text-capitalize"> Dúvidas </span>
                </v-row>
              </div>
            </v-btn>
            </template>
            <template v-slot:default="dialog">
              <v-card>
                <v-toolbar
                  color="primary"
                  dark
                >Como utilizar</v-toolbar>
                <v-divider></v-divider>
                <v-card-text>
                <div class="text-subtitle-2 pa-1">
                <span>
                  <b>• O que é</b><br><br>
                  O Transtorno obsessivo-compulsivo (TOC) é um tipo de ansiedade caracterizada pela presença de <u>obsessões</u> e <u>compulsões</u>. Mas o que será isto? 
                  As obsessões são pensamentos, impulsos ou imagens recorrentes e persistentes que são vivenciados como intrusivos e indesejados. Já as compulsões são comportamentos repetitivos ou atos mentais que um indivíduo se sente compelido a executar em resposta a uma obsessão ou de acordo com regras que devem ser aplicadas rigidamente. 
                  O TOC se difere das preocupações e rituais típicos por serem excessivos e persistirem além dos períodos apropriados. Por isso, o diagnóstico requer a avaliação de inúmeros fatores, incluindo o nível de sofrimento do indivíduo e o prejuízo no seu funcionamento.
                </span>
                </div>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                  text
                  @click="dialog.value = false"
                >Fechar</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="6">
        <v-dialog
          transition="dialog-top-transition"
          scrollable
          max-width="600"
          >
            <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="blue-grey darken-1"
              class="ma-2 white--text"
              fab
              tile
              text
              v-bind="attrs"
              v-on="on"
              width="150px"
              height="150px"
            >
              <div>
                <v-row>
                  <div class="mt-3">
                    <v-img
                      width="85px"
                      src="../assets/checklist.png"
                    ></v-img>
                  </div>
                </v-row>
                <v-row class="justify-center">
                  <span class="mt-3 mr-2 text-capitalize"> Check List  </span>
                </v-row>
              </div>
            </v-btn>
            </template>
            <template v-slot:default="dialog">
              <v-card>
                <v-toolbar
                  color="primary"
                  dark
                >Check List</v-toolbar>
                <v-divider></v-divider>
                <v-card-text>
                <div class="text-subtitle-2 pa-1">
                <check-list />
                </div>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                  text
                  @click="dialog.value = false"
                >Fechar</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
      <v-col cols="6">
        <v-dialog
          transition="dialog-top-transition"
          scrollable
          max-width="600"
          >
            <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="blue-grey darken-1"
              class="ma-2 white--text"
              fab
              tile
              text
              v-bind="attrs"
              v-on="on"
              width="150px"
              height="150px"
            >
              <div>
                <v-row>
                  <div class="mt-3 ml-2">
                    <v-img
                      width="95px"
                      src="../assets/diario.png"
                    ></v-img>
                  </div>
                </v-row>
                <v-row class="justify-center">
                  <span class="mt-4 ml-4 text-capitalize"> Meu diário  </span>
                </v-row>
              </div>
            </v-btn>
            </template>
            <template v-slot:default="dialog">
              <v-card>
                <v-toolbar
                  color="primary"
                  dark
                >Meu diário</v-toolbar>
                <v-divider></v-divider>
                <v-card-text>
                <div class="text-subtitle-2 pa-1">
                <MeuDiario />
                </div>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                  text
                  @click="dialog.value = false"
                >Fechar</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="6">
        <v-dialog
          transition="dialog-top-transition"
          scrollable
          max-width="600"
          >
            <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="blue-grey darken-1"
              class="ma-2 white--text"
              fab
              tile
              text
              v-bind="attrs"
              v-on="on"
              width="150px"
              height="150px"
            >
              <div>
                <v-row>
                  <div class="mt-5">
                    <v-img
                      width="140px"
                      src="../assets/acalmar.png"
                    ></v-img>
                  </div>
                </v-row>
                <v-row class="justify-center">
                  <span class="mt-5 text-capitalize"> Me acalmar  </span>
                </v-row>
              </div>
            </v-btn>
            </template>
            <template v-slot:default="dialog">
              <v-card>
                <v-toolbar
                  color="primary"
                  dark
                >Playlists</v-toolbar>
                <v-divider></v-divider>
                <v-card-text>
                <div class="text-subtitle-2 pa-1">
                <playlist />
                </div>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                  text
                  @click="dialog.value = false"
                >Fechar</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
      <v-col cols="6">
        <v-dialog
          transition="dialog-top-transition"
          scrollable
          max-width="600"
          >
            <template v-slot:activator="{ on, attrs }">
            <v-btn
              color="blue-grey darken-1"
              class="ma-2 white--text"
              fab
              tile
              text
              v-bind="attrs"
              v-on="on"
              width="150px"
              height="150px"
            >
              <div>
                <v-row>
                  <div class="mt-3 ml-2">
                    <v-img
                      width="100px"
                      src="../assets/tempo.png"
                    ></v-img>
                  </div>
                </v-row>
                <v-row class="justify-center">
                  <span class="mt-3 text-capitalize"> Tempo de uso  </span>
                </v-row>
              </div>
            </v-btn>
            </template>
            <template v-slot:default="dialog">
              <v-card>
                <v-toolbar
                  color="primary"
                  dark
                >Tempo de uso</v-toolbar>
                <v-divider></v-divider>
                <v-card-text>
                <div class="text-subtitle-2 pa-1">
                <TempoDeUso />
                </div>
              </v-card-text>
              <v-card-actions class="justify-end">
                <v-btn
                  text
                  @click="dialog.value = false"
                >Fechar</v-btn>
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import Vue from "vue";
import { Component } from "vue-property-decorator";
import Playlist from "./Playlist.vue";
import CheckList from "./CheckList.vue";
import TempoDeUso from "./TempoDeUso.vue";
import MeuDiario from "./MeuDiario.vue";


@Component({
  components:{
    Playlist,
    CheckList,
    TempoDeUso,
    MeuDiario
  },
})

export default class Menu extends Vue {

  

}
</script>
