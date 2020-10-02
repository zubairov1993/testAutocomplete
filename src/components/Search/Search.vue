<template>
  <div class="search">
    <div class="search__block">
      <input 
        type="text" 
        v-model="state" 
        autocomplete="off" 
        @focus="modal = true"
        class="search__input"
        placeholder="Хочу найти..."        
      >
      <button>
        <i class="fas fa-search" v-if="!modal"></i>
      </button>
      <button>
        <i class="fas fa-times" v-if="modal" @click="close"></i>
      </button>
    </div>
    <div v-if="filteredStates && modal">
      <ul class="search__list">
        <li 
          v-for="filteredState in filteredStates" 
          v-bind:key="filteredState" 
          @click="setState(filteredState)"
          class="search__list_item"
          placeholder="saw"
          >{{ filteredState }}</li>
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
        'Аккумуляторный инструмент', 
        'Бороздоделы (штроборезы)', 
        'Гайковерты', 
        'Гвоздезабиватели (степлеры)', 
        'Граверы',
        'Дрели', 
        'Заклепочники', 
        'Измерительный инструмент', 
        'Лобзики'
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
    },
    close() {
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
@import '../../assets/variables';
@import './Search';
</style>