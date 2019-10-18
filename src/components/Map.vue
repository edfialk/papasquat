<template>
    <div class="map" />
</template>

<script>

import gmapsInit from '../utils/gmaps';

export default {
    async mounted() {
        try {
            const google = await gmapsInit();
            const map = new google.maps.Map(this.$el, {
                center: {lat: -34.397, lng: 150.644},
                zoom: 8
            });
        } catch (err) {
            console.error(err);
        }
    }
    
}
</script>

<style lang="scss" scoped>
.map {
    width: 100vw;
    height: 100vh;
}
</style>