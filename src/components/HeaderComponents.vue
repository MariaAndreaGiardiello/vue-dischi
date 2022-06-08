<template>
  <header>
      <div class="container-fluid">
          <div class="row">
                <div class="col-11">
                  <div class="logo-box">
                        <img class="img-fluid" src="../assets/img/spotify-logo.png" alt="">
                  </div>
                </div>
          </div>
      </div>
  </header>
</template>
<script src="https://kit.fontawesome.com/bec049b842.js" crossorigin="anonymous"></script>
<script>
export default {
    name: 'HeaderComponents',
}
</script>

<style lang="scss" scoped>
header {
    background-color: var(--primary-color);
}

.logo-box {
    width: 50px;
    height: 50px;
    line-height: 45px;
}
</style>