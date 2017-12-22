<template>
  <div class="filters col-sm-4" v-bind:class="{ hidden: hideFilters }">
    <div class="row filter-heading">
      <div class="col-sm-6 heading"><h5>Filters</h5></div>
      <div class="col-sm-6 close"><i class="material-icons close-filters" @click="showHide">highlight_off</i></div>
    </div>
    <div class="row filter-heading">
        <FilterByLocation />
    </div>
    <div class="row filter-heading">
        <FilterByPrice />
    </div>
    <div class="row filter-heading">
        <FilterBySquare />
    </div>
    <div class="row filter-heading">
        <FilterByType />
    </div>
    <div class="row filter-heading">
        <FilterBySize />
    </div>
    <div class="row filter-heading">
        <FilterByTakeDate />
    </div>
    <div class="row filter-heading">
        <FilterByRentalPeriod />
    </div>
    <div class="row filter-heading">
        <FilterByFurnish />
    </div>
    <div class="row filter-heading">
        <FilterByRequirement />
    </div>
    <div class="row filter-heading">
        <FilterByCaseNumber />
    </div>
  </div>
</template>

<script>
import FilterByLocation from '../components/Filters/FilterByLocation'
import FilterByPrice from '../components/Filters/FilterByPrice'
import FilterBySquare from '../components/Filters/FilterBySquare'
import FilterByType from '../components/Filters/FilterByType'
import FilterBySize from '../components/Filters/FilterBySize'
import FilterByTakeDate from '../components/Filters/FilterByTakeDate'
import FilterByRentalPeriod from '../components/Filters/FilterByRentalPeriod'
import FilterByFurnish from '../components/Filters/FilterByFurnish'
import FilterByRequirement from '../components/Filters/FilterByRequirement'
import FilterByCaseNumber from '../components/Filters/FilterByCaseNumber'
export default {
  name: 'Filters',
  components: {
    FilterByLocation, FilterByPrice,
    FilterBySquare, FilterByType, FilterBySize, FilterByTakeDate,
    FilterByRentalPeriod, FilterByFurnish, FilterByRequirement, FilterByCaseNumber
  },
  props: {
     hideFilters: {
       type: Boolean,
     }
  },
  data(){
    return {
      isHidden: false,
    }
  },
  methods: {
    showHide: function(){
      this.isHidden = true;
      this.$emit('update', this.isHidden);
    }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .hidden{
    display:none;
  }

  .filters{

    .filter-heading{
      padding-top: 15px;
      padding-bottom: 15px;
      border-bottom: 1px solid #e6e6e6;

      .heading{
        text-align: left;
      }
      .close{
        text-align: right;
        .close-filters{
          opacity: 0.3;
        }
        .close-filters:hover{
              cursor: pointer;
        }
      }

    }


  }

</style>
