<template>
    <div>
        <v-card>
            <div class ="pa-2">
                <v-textarea
                outlined
                label="Registro diário"
                v-model="registro"
                ></v-textarea>
                <v-card-actions class="justify-end">
                    <v-btn small color="primary" @click="cadastrarRegistro()">Cadastrar</v-btn>
                </v-card-actions>
            </div>
        </v-card>
        <div class="pa-5">
            <span>Lista de registros diários</span>
        </div>
        <div class="mt-2" v-for="registroDiario in this.listaDeRegistro" :key="`${registroDiario.data}`">
            <v-expansion-panels>
                <v-expansion-panel>
                    <v-expansion-panel-header>
                        <div max-width="239">
                            {{ registroDiario.data}}
                        </div>
                        <template v-slot:actions>
                            <v-icon color="teal">mdi-check</v-icon>
                        </template>
                    </v-expansion-panel-header>
                    <v-expansion-panel-content>
                        <div class="pa-1">
                        <v-row>
                            {{ registroDiario.registro}}
                        </v-row>   
                        <v-row class="float-right">
                            <v-dialog
                            transition="dialog-top-transition"
                            scrollable
                            max-width="600"
                            v-model="dialog"
                            >
                                <template v-slot:activator="{ on, attrs }">
                                    <v-btn v-on="on" v-bind="attrs" small color="primary" @click="editarRegistro(registroDiario.registro)">Atualizar</v-btn>
                                </template>
                                <template>
                                <v-card>
                                    <v-toolbar
                                    color="primary"
                                    dark
                                    >Editar Registro</v-toolbar>
                                    <v-divider></v-divider>
                                    <v-card-text>
                                        <v-textarea
                                        class="mt-4"
                                        outlined
                                        label="Registro diário"
                                        v-model="registroEditar"
                                        ></v-textarea>
                                    </v-card-text>
                                    <v-card-actions class="justify-end">
                                        <v-btn
                                        text
                                        @click="editarRegistroFinal(registroDiario.data)"
                                        >Finalizar</v-btn>
                                    </v-card-actions>
                                </v-card>
                            </template>
                            </v-dialog>
                        </v-row>
                        </div>
                    </v-expansion-panel-content>
                </v-expansion-panel>
            </v-expansion-panels>
        </div>
    </div>
</template>

<script lang="ts">
import Vue from "vue";
import moment from 'moment';
import { ListaDeRegistro } from "../model/ListaDeRegistro";
import { Component } from "vue-property-decorator";

@Component({
  components:{
  },
})

export default class MeuDiario extends Vue {
    public registro: string = "";
    public registroEditar: string = "";
    public listaDeRegistro: ListaDeRegistro[] = []
    public dialog: boolean = false;

    public async mounted() {
        this.carregarlista();
    }

    public carregarlista(){
        this.listaDeRegistro.push({ data: "domingo, 20 junho 2021", registro: "Neste dia houve um almoço de família na casa dos meus avós e fiquei desconfortável com a presença de algumas pessoas."});
        this.listaDeRegistro.push({ data: "segunda, 21 junho 2021", registro: "Foi um dia comum, muita pressão no trabalho e fiquei ansioso com isso... mas consegui lidar."});
        this.listaDeRegistro.push({ data: "terça, 22 junho 2021", registro: "Hoje o dia foi tranquilo."});
        this.listaDeRegistro.push({ data: "quarta, 23 junho 2021", registro: "Não tive uma boa noite de sono e por isso me atrasei para o trabalho."});
        this.listaDeRegistro.push({ data: "quinta, 24 junho 2021", registro: "Tudo tranquilo até o momento."});
        this.listaDeRegistro.push({ data: "sexta, 25 junho 2021", registro: "Fui convidado pelos colegas do trabalho à um happy hour, porém não sabia como me comportar na preseça de mais pessoas."});
    }

    public cadastrarRegistro(){
        moment.locale('pt-br');

        const dataAtual = moment().format('dddd, DD MMMM YYYY');
        const procurarRegistro = this.listaDeRegistro.findIndex(r => r.data == dataAtual);

        if (this.registro !== "" && procurarRegistro == -1){
            this.listaDeRegistro.push({ data: dataAtual, registro: this.registro});
            this.registro = "";
        }
        else{
            return;
        }
        
    }

    public editarRegistro(registroAtual: string){
        this.registroEditar = registroAtual;
        return;
    }
    public editarRegistroFinal(dataAtual: string){
        const procurarRegistro = this.listaDeRegistro.findIndex(r=> r.data == dataAtual);
        this.listaDeRegistro[procurarRegistro].registro = this.registroEditar;
        return this.dialog = false;
    }

}
</script>

<style>
</style>