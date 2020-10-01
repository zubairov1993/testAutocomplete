<template>
  <div class="head">
    <div class="head__wrapper">
      <div class="head__logo">
        <img src="../assets/Group.png" alt="logo">
      </div>
      <div class="head__block">
      <button class="head__block_catalog"><i class="fas fa-bars"></i>Каталог</button>
      <Search2 />
      <button class="head__block_list"><i class="far fa-list-alt"></i>Список</button>
      </div>
    </div>
  </div>
</template>

<script>
import Search2 from './Search2'

export default {
  components: {
    Search2
  }
}
</script>

<style scoped lang="scss">
.head{
  background: #ffffff;
  &__wrapper{
    height: 76px;
    max-width: 1100px;
    margin: 0 auto;
    display: flex;
  }
  &__block{
    display: flex;
    &_catalog{
      width: 116px;
      height: 40px;
      background: #FED83D;
      border: none;
      border-radius: 4px;
      font-size: 14px;
      font-family: 'Open Sans', sans-serif;
      font-weight: 600;
      outline: none;
      i{
        padding-right: 10px;
      }
    }
    &_list{
      width: 111px;
      height: 40px;
      background: #FAFBFC;
      border: 1px solid #ECEFF1;
      border-radius: 4px;
      font-size: 14px;
      font-family: 'Open Sans', sans-serif;
      font-weight: 600;
      outline: none;
      i{
        padding-right: 10px;
        font-size: 20px;
      }
    }
  }
}
</style>
