<template>
  <section>
      <div class="container">
          <div class="row justify-content-center">
              <div class="col-12">
                  <FilterSearchVue @searching="songGenre"/>
              </div>
          </div>
          <div class="row justify-content-center">
                <album-covers class= "col-6 col-sm-4 col-md-3 col-lg-2 m-3" v-for="(album, index) in albumsGenre" :key="index" :album="album"/>
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
            albumsGenre: [],
        };
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((response) => {
            this.albums = response.data.response;
            this.albumsGenre = response.data.response;
        })
            .catch((error) => {
            console.log(error);
        });
    },
    components: { 
        AlbumCovers, 
        FilterSearchVue, 
    },
    methods: {
        songGenre(searchText) {
            this.albumsGenre = this.albums.filter((elm) => elm.genre.toLowerCase().includes(searchText.toLowerCase()))
        }
    },
}

</script>

<style lang="scss" scoped>

</style>