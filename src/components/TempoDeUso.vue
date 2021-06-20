<template>
    <div>
        <v-container fluid>
            <v-sparkline
            :value="value"
            :gradient="gradient"
            line-width="10"
            type="bar"
            auto-line-width="true"
            auto-draw
            show-labels="true"
            label-size="10"
            :labels="semana"
            width="200"
            ></v-sparkline>
        </v-container>
        <div>
            <v-card
            color="green"
            dark
            class="mt-6 pr-3"
            >
                <v-row>
                    <v-col cols="9">
                        <v-card-title class="body-2">Horas Semanais</v-card-title>
                        <v-card-subtitle class="caption">Horas usando o aplicativo na semana, meta de 3hrs dia.</v-card-subtitle>
                    </v-col>
                    <v-col cols="3">
                        <v-progress-circular size="50" class="mt-5" value="67">14/21</v-progress-circular>
                    </v-col>
                </v-row>
            </v-card>

            <v-card
            color="amber"
            dark
            class="mt-6 pr-3"
            >
                <v-row>
                    <v-col cols="9">
                        <v-card-title class="body-2">Recompensas</v-card-title>
                        <v-card-subtitle class="caption">Conforme vai conquistando estrelas sua porcentagem vai aumentando.</v-card-subtitle>
                    </v-col>
                    <v-col cols="3">
                        <v-progress-circular size="50" class="mt-8" value="30">3/10</v-progress-circular>
                    </v-col>
                </v-row>
            </v-card>
            <v-card
            color="grey"
            dark
            class="mt-6 pr-3"
            >   
                <div class="pa-3">
                    <v-row>
                        <v-card-title class="body-2">Suas Conquistas</v-card-title>
                    </v-row>
                    <v-row>
                        <div class="mb-1 ml-3">
                            <v-icon large color="amber">mdi-trophy</v-icon>
                            <v-icon large color="amber">mdi-trophy</v-icon>
                        </div>
                    </v-row>
                </div>
            </v-card>
        </div>
    </div>
</template>

<script lang='ts'>
import Vue from "vue";
import { Component } from "vue-property-decorator";

@Component({
  components:{
  },
})

export default class TempoDeUso extends Vue {
    public value: number [] = [4, 2, 1, 3, 1, 3, 0];
    public gradient: string[] = ["purple", "violet"];
    public semana: any[] = ["Dom", "Seg", "Ter", "Qua", "Qui", "Sex", "Sab"];
}
</script>

<style>
</style>