<template>
    <div class="search pa-2">
        <v-text-field
            v-model="search"
            placeholder="Search Papa Squat"
            :outlined=false
            :solo=true
            :clearable=true
            :loading="loading"
            :hide-details=true
        >
            <template v-slot:prepend-inner>
                <v-icon @click="showMenu">mdi-menu</v-icon>
            </template>
            <template v-slot:append>
                <v-icon @click="doSearch">mdi-magnify</v-icon>
            </template>
        </v-text-field>
    </div>
</template>

<script>
export default {
    data() {
        return {
            search: "",
            loading: false
        }
    },

    methods: {
        doSearch() {
            console.log('do search');
        },

        showMenu() {
            console.log('show menu');
        }
    }
}
</script>

<style lang="scss">
.search {
    .v-text-field__slot {
        border-left: 1px solid rgba(0, 0, 0, 0.24);
        padding-left: 8px;
    }
    .v-text-field .v-input__prepend-inner {
        padding-right: 8px;
    }
}
</style>