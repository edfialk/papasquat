<template>
    <v-list two-line class="overflow-y">
        <template v-for="item in 20">

                <v-list-item :key="item">
                    <v-list-item-content>
                        <v-skeleton-loader
                            :loading="loading"
                            transition="fade-transition"
                            height="94"
                            type="list-item-two-line">
                            <v-list-item-title>title</v-list-item-title>
                        </v-skeleton-loader>
                    </v-list-item-content>
                    <!-- <v-list-item-subtitle class="text--primary" v-text="item." -->
                </v-list-item>

        </template>
    </v-list>
</template>

<script>

export default {

    data: () => ({
        items: [
            { title: "test" }
        ],
        loading: true,
    }),

    created() {
        // window.setTimeout(() => {
        //     this.loading = false
        // }, 2000);
    }


}

</script>

<style lang="scss">
    .v-list-item + .v-list-item {
        border-top: 1px solid rgba(0, 0, 0, 0.12);
    }
</style>