<template>
    <v-app-bar app clipped-left color="white">
        <v-toolbar-title class="logo">
            <nuxt-link to="/">
                <img src="/logo.png" alt class="block h-10 mx-auto mr-4 mt-2" />
            </nuxt-link>
        </v-toolbar-title>
        <v-spacer />
        <v-btn icon>
            <v-icon color="black">mdi-apps</v-icon>
        </v-btn>
    </v-app-bar>
</template>

<style>
.logo {
    align-self: center;
}
</style>