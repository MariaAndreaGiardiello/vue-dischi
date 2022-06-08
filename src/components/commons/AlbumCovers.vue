<template>
  <div class="album-box">
      <div class="album-cover">
          <img class="img-fluid" :src="album.poster" alt="">
      </div>
      <h5 class="song-title">{{album.title}}</h5>
      <h6 class="author-year">{{album.author}} <br> {{album.year}}</h6>
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
}

.song-title {
    color: var(--song-title-color);
    text-align: center;
    text-transform: uppercase;
    margin-top: 30px;
}

.author-year {
    color: var(--song-author-year);
    text-align: center;
    text-transform: uppercase;
    font-size: 12px;
    margin: 15px auto;
}

.album-cover {
    width: 160px;
    height: 160px;
    margin: 15px auto;
}
</style>