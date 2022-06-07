<template>
  <div class="album-box">
      <div class="album-cover">
          <img class="img-fluid" :src="album.poster" alt="">
      </div>
      <h4 class="song-title">Titolo Canzone</h4>
      <h5 class="author-year">Autore e Anno</h5>
  </div>
</template>

<script>
export default {
    name: 'AlbumCovers',
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
.album-box {
    background-color: var(--primary-color);
    height: 300px;  
}

.album-cover {
    margin: 15px 10px;
    width: 150px;
    height: 100px;
}
</style>