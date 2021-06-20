<template>
    <div>
        <v-card>
            <div class ="ma-2">
                <v-text-field
                v-model="itemLista"
                label="Cadastrar item"
                required
                ></v-text-field>
                <v-card-actions class="justify-end">
                    <v-btn small color="primary" @click="cadastrarItem()">Cadastrar</v-btn>
                </v-card-actions>
            </div>
        </v-card>
        <div class="justify-center">
            <span>Listagem dos itens</span>
        </div>
        <div v-for="item in this.lista" :key="`${item.nome}`">
        <v-row>
            <v-col cols="11">
                <v-checkbox v-model="item.status" :label="item.nome"></v-checkbox>
            </v-col>
            <v-col cols="1">
                <v-icon class="float-right mt-5" color="red" @click="removerItem(item.nome)">mdi-close</v-icon>
            </v-col>
        </v-row>
        </div>
    </div>
</template>

<script lang='ts'>
import Vue from "vue";
import { Component } from "vue-property-decorator";
import { Lista } from "../model/Lista";

@Component({
  components:{
  },
})

export default class CheckList extends Vue {
    public lista: Lista[] = [];
    public itemLista = "";
    public item1 = false;

    public async mounted() {
        this.carregarlista();
    }

    public carregarlista(){  
        this.lista.push({ nome: "Fechar a porta", status: false});
        this.lista.push({ nome: "Apagar a Luz", status: false});
        this.lista.push({ nome: "Fechar janelas", status: true});
    }

    public cadastrarItem(){
        if (this.itemLista !== ""){
            this.lista.push({ nome: this.itemLista, status: false});
            this.itemLista = "";
        }
        else{
            return;
        }
    }

    public removerItem(itemLista: string){
        const procurarItem = this.lista.findIndex(item => item.nome == itemLista);
        this.lista.splice(procurarItem, 1);
    }
}
</script>

<style>
</style>