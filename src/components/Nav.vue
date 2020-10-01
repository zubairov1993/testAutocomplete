<template>
  <div class="nav">
    <div class="nav__wrapper">
      <div class="nav__place">
        <i class="fas fa-map-marker-alt"></i>
        <p>Вогоградская область</p>
      </div>
      <div class="nav__list">
        <ul>
          <li><a href="">Тендеры</a></li>
          <li><a href="">Базы подрядчиков</a></li>
          <li>
            <select>
              <option value="">Другие сервисы</option>
              <option value="">Другие сервисы</option>
              <option value="">Другие сервисы</option>
            </select>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.nav{
  background: #FAFBFC;
  border-bottom: 1px solid #ECEFF1;
  &__wrapper{
    max-width: 1100px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 32px;
  }
  &__place{
    display: flex;
    p{
      padding-left: 10px;
      font-family: 'Open Sans', sans-serif;
      font-size: 12px;
      font-weight: 400;
      color: #708598;
    }
    i{
      font-size: 12px;
      padding-top: 3px;
      color: #708598;
    }
  }
  &__list ul{
    display: flex;
    li{
      list-style: none;
      padding-left: 10px;
      font-family: 'Open Sans', sans-serif;
      font-size: 12px;
      font-weight: 400;
      a{
        text-decoration: none;
        color: #708598;
      }
      select{
        border: none;
        font-family: 'Open Sans', sans-serif;
        font-size: 12px;
        font-weight: 400;
        color: #708598;
        background: #FAFBFC;
        margin-top: -1px;
      }
    }
  }
}
</style>
