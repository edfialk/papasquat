<template>

    <div class="filters white--text">
        <div class="d-flex pa-2">
        <!-- <VContainer class="d-flex align-items-center"> -->

            <VSelect
                :items="countItems"
                v-model="count"
                class="mx-2 caption pt-0 mt-0"
                dense
                hide-details
                dark
            ></VSelect>

            <VSelect
                :items="orderItems"
                v-model="order"
                class="mx-2 caption pt-0 mt-0"
                dense
                hide-details
                dark
            ></VSelect>

            <VSelect
                :items="typeItems"
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
        countItems: [10, 20, 50, "All"],
        order: "Closest",
        orderItems: ["Closest", "Best"],
        type: "Spots",
        typeItems: ["Spots", "Parks", "Restaurants", "Bars"],
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
        // text-align: center;
    }
}
.v-icon.v-icon.fs-18 {
    font-size: 19px;
}

</style>