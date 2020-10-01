<template>
  <div class="search">
    <ejs-autocomplete :dataSource='dataItem' :fields='dataFields' placeholder='Select a Game'>

    </ejs-autocomplete>
  </div>
</template>

<script>
import Vue from 'vue';
import { AutoCompletePlugin } from '@syncfusion/ej2-vue-dropdowns';
Vue.use(AutoCompletePlugin);
export default Vue.extend({
  data: function() {
    return {
      dataItem: [
        { Id: 'Game1', Game: 'Football' },
        { Id: 'Game2', Game: 'Basketball'},
        { Id: 'Game3', Game: 'Volleyball'},
        { Id: 'Game4', Game: 'Baseball' },
        { Id: 'Game5', Game: 'Badminton'}
      ],
      dataFields: {value: 'Game'}
    }
  }
})
</script>

<style scoped lang="scss">
@import url(http://cdn.syncfusion.com/ej2/material.css);
ejs-autocomplete{
  border: none;
}
</style>
