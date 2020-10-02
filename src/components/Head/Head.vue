<template>
  <div class="head">
    <div class="head__wrapper">
      <div class="head__logo">
        <img src="../../assets/Group.png" alt="logo">
      </div>
      <div class="head__block">
        <button class="head__block_catalog"><i class="fas fa-bars"></i>Каталог</button>
        <Search />
        <button class="head__block_list"><i class="far fa-list-alt"></i>Список</button>
        <div class="head__block_circle">
          <p>A</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Search from '../Search/Search'

export default {
  components: {
    Search
  }
}
</script>

<style scoped lang="scss">
@import '../../assets/variables';
@import './Head';
</style>
