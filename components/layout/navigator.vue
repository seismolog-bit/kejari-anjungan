<template>
    <v-navigation-drawer permanent app clipped>
        <v-list shaped>
            <v-subheader>Layanan</v-subheader>
            <v-list-item-group v-model="item" color="success">
                <v-list-item v-for="(item, i) in items" :key="i" :to="item.link" link>
                    <v-list-item-icon>
                        <v-icon v-text="item.icon"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    props: {
        source: String
    },
    data: () => ({
        drawer: true,
        item: 0,
        items: [
            // { text: "Beranda", icon: "mdi-home", link: "/" },
            {
                text: "Tilang Drive Thru",
                icon: "mdi-motorbike",
                link: "/layanan/tilang-drive-thru"
            },
            {
                text: "Izin Besuk Tahanan",
                icon: "mdi-alarm-bell",
                link: "/layanan/besuk-tahanan"
            }
        ]
    })
};
</script>

<style>
#keep .v-navigation-drawer__border {
    display: none;
}
</style>