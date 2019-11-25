<template>

    <div class="filters white--text">
        <div class="d-flex pa-2">
        <!-- <VContainer class="d-flex align-items-center"> -->

            <VSelect
                :items="counts"
                v-model="count"
                class="mx-2 caption pt-0 mt-0"
                dense
                hide-details
                dark
            ></VSelect>

            <VSelect
                :items="orders"
                v-model="order"
                class="mx-2 caption pt-0 mt-0"
                dense
                hide-details
                dark
            ></VSelect>

            <VSelect
                :items="types"
                v-model="type"
                class="mx-2 caption pt-0 mt-0"
                dense
                hide-details
                dark
            ></VSelect>
        </div>
        <div class="pa-2 py-3 d-flex justify-end blue darken-3 text-uppercase align-center">
            <VIcon color="white" class="fs-18">mdi-tune</VIcon>
            <div class="mx-2">More Filters</div>
            <div class="mx-2">Reset</div>

        </div>

        <!-- </VContainer> -->
    </div>

</template>

<script>
export default {
    data: () => ({
        count: 10,
        counts: [10, 20, 50, "All"],
        order: "Closest",
        orders: ["Closest", "Best"],
        type: "Spots",
        types: ["Spots", "Parks", "Restaurants", "Bars"],
    })
}
</script>

<style lang="scss">

.filters {
    font-size: 13px !important;
    color: #fff !important;
    .v-text-field > .v-input__control > .v-input__slot:after {
        border: 0;
    }
    .small {
        width: 80px;
    }
}
.v-icon.v-icon.fs-18 {
    font-size: 19px;
}

</style>