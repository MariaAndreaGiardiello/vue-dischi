<template>
  <section>
      <div class="container">
          <div class="row">
                <album-covers class="col-4" v-for="(albums, index) in albums" :key="index"/>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import AlbumCovers from '../commons/AlbumCovers.vue';
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
            this.albums = response.data;
        })
            .catch((error) => {
            console.log(error);
        });
    },
    components: { AlbumCovers }
}

</script>

<style lang="scss" scoped>

</style>