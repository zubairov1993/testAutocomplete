<template>
  <div class="search">
    <div class="search__block">
      <input 
        type="text" 
        v-model="state" 
        autocomplete="off" 
        @focus="modal = true"
        class="search__input"
      >
      <i class="fas fa-search"></i>
    </div>
    <div v-if="filteredStates && modal">
      <ul class="search__list">
        <li 
          v-for="filteredState in filteredStates" 
          v-bind:key="filteredState" 
          @click="setState(filteredState)"
          class="search__list_item"
          ><a href="#">{{ filteredState }}</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      state: '',
      modal: false,
      states: [
        'Аккумуляторный инструмент', 'Kazan', 'Ufa', 'Piter', 'London'
      ],
      filteredStates: []
    }
  },
  mounted() {
    this.filterStates();
  },
  methods: {
    filterStates() {
      if(this.state.length === 0) {
        this.filteredStates = this.states;
        this.model = false;
      }
      this.filteredStates = this.states.filter(state => {
        return state.toLowerCase().startsWith(this.state.toLowerCase());
      })
    },
    setState(state) {
      this.state = state;
      this.modal = false;
    }
  },
  watch: {
    state() {
      this.filterStates();
    }
  }
}
</script>

<style scoped lang="scss">
.search{
  width: 526px;
  height: 40px;
  border: 1px solid #ECEFF1;
  border-radius: 4px;
  &__block{
    display: flex;
    align-items: center;
  }
  &__input{
    width: 500px;
    height: 40px;
    border: none;
    outline: none;
  }
  &__list{
    border: 1px solid #ECEFF1;
    &_item{
      list-style: none;
      border-bottom: 1px solid #ECEFF1;
      border-radius: 4px;
      height: 40px;
      display: flex;
      align-items: center;
      padding-left: 20px;
    }
    &_item:last-child{
      border-bottom: none;
    }
  }
  
  i{
    font-size: 20px;
    color: #708598;
    padding-right: 10px;
  }
}
</style>