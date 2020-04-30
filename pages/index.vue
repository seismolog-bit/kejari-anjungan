<template>
    <div>
        <v-row class="container--fluid ma-3 fill-height">
            <v-carousel cycle hide-delimiter-background show-arrows-on-hover height="48vh">
                <v-carousel-item v-for="(slide, i) in slides" :key="i">
                    <v-sheet :color="colors[i]" height="100%">
                        <v-row class="fill-height" align="center" justify="center">
                            <div class="display-3">{{ slide }} Slide</div>
                        </v-row>
                    </v-sheet>
                </v-carousel-item>
            </v-carousel>
        </v-row>
        <v-row :align="alignment" :justify="justify" class="ma-1">
            <v-col v-for="card in cards" :key="card.title" :cols="card.flex">
                <v-card
                    dark
                >
                    <v-img
                        :src="card.src"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                    >
                        <!-- <v-card-title v-text="card.title"></v-card-title> -->
                        <v-card-title class="headline" v-text="card.title"></v-card-title>

                        <v-card-subtitle v-text="card.subtitle"></v-card-subtitle>

                        <v-card-actions>
                            <v-btn text>Detail layanan</v-btn>
                        </v-card-actions>
                    </v-img>
                </v-card>
            </v-col>
        </v-row>
    </div>
</template>

<style>
</style>

<script>
export default {
    data() {
        return {
            colors: [
                "indigo",
                "warning",
                "pink darken-2",
                "red lighten-1",
                "deep-purple accent-4"
            ],
            slides: ["First", "Second", "Third", "Fourth", "Fifth"],
            alignment: "center",
            justify: "space-between",
            cards: [
                {
                    title: "Supermodel",
                    subtitle: "Listen to your favorite artists and albums whenever and wherever, online and offline.",
                    src: "https://cdn.vuetifyjs.com/images/cards/foster.jpg",
                    flex: 3
                },
                {
                    title: "Halcyon Days",
                    subtitle: "Listen to your favorite artists and albums whenever and wherever, online and offline.",
                    src: "https://cdn.vuetifyjs.com/images/cards/halcyon.png",
                    flex: 3
                },
                {
                    title: "Favorite road trips",
                    subtitle: "Listen to your favorite artists and albums whenever and wherever, online and offline.",
                    src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
                    flex: 3
                },
                {
                    title: "Best airlines",
                    subtitle: "Listen to your favorite artists and albums whenever and wherever, online and offline.",
                    src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
                    flex: 3
                }
            ]
        };
    }
};
</script>