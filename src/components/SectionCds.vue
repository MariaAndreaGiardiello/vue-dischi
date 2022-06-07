<template>
  <section></section>
</template>

<script>
import axios from 'axios';
export default {
    name: 'SectionCds',
    data () {
        return {
            albums: [],
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data;
        })
        .catch((error) => {
            console.log(error);
        })
    }
}

</script>

<style lang="scss" scoped>

</style>