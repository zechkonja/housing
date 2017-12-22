
<template>
  <div class="filterByTakeDate col-sm-12">
    <div class="heading">Overtagelsesdato</div>
    <datepicker v-model="date" input-class="test"></datepicker>
  </div>
</template>

<script>
import Datepicker from 'vuejs-datepicker';



export default {
  name: 'FilterByTakeDate',
  data(){
    return {
      date: new Date(),
      config: {
          format: 'DD/MM/YYYY',
      }
    }
  },
  components: {
      Datepicker
  },
  methods: {
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

    .filterByTakeDate{
        margin: 0;
        .heading{
            text-align: left;
            font-weight: bold;
        }
    }



</style>
