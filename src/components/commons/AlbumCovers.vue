<template>
  <div class="album-box">
      <div class="album-cover"></div>
      <h4 class="song-title">Titolo Canzone</h4>
      <h5 class="author-year">Autore e Anno</h5>
  </div>
</template>

<script>
export default {
    name: 'AlbumCovers'
}
</script>

<style lang="scss" scoped>
.album-box {
    background-color: var(--primary-color);
    height: 300px;
    
}
</style>