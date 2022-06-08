<template>
  <section>
      <div class="container">
          <div class="row justify-content-center">
              <div class="col-12">
                  <FilterSearchVue/>
              </div>
          </div>
          <div class="row justify-content-center">
                <album-covers class= "col-6 col-sm-4 col-md-3 col-lg-2 m-3" v-for="(album, index) in albums" :key="index" :album="album"/>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import AlbumCovers from '../commons/AlbumCovers.vue';
import FilterSearchVue from '../commons/FilterSearch.vue';
export default {
    name: "SectionCds",

    data() {
        return {
            albums: [],
        };
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((response) => {
            this.albums = response.data.response;
            console.log(response.data.response);
        })
            .catch((error) => {
            console.log(error);
        });
    },
    components: { AlbumCovers, FilterSearchVue, }
}

</script>

<style lang="scss" scoped>

</style>