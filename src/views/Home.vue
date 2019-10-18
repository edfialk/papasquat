<template>
  <div>

    <v-navigation-drawer
      fixed
      permanent
      width="400"
      bottom
    >
      <div class="d-flex flex-column h-100">
        <div class="blue darken-1">
          <Search></Search>
          <Filters></Filters>
        </div>
        <ItemList></ItemList>
      </div>
    </v-navigation-drawer>

    <v-content>
      <Map></Map>
    </v-content>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      test
    </v-navigation-drawer>

  </div>
</template>

<script>
import Map from '../components/Map';
import Search from '../components/Search';
import Filters from '../components/Filters';
import ItemList from '../components/ItemList';

export default {
  components: {
    Map, Search, ItemList, Filters
  },

  data: () => ({
    drawer: false
  })
};
</script>
