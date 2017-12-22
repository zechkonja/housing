<template>
  <div class="filterBySquare col-sm-12">
    <div class="heading">Boligareal <span class="subtitle">m2 (bbr)</span></div>
    <vue-slider v-model="value"  v-bind="options"></vue-slider>
    <span class="minPrice">{{minValue}}</span><span class="maxPrice">{{maxValue}}</span>
  </div>
</template>

<script>

import vueSlider from 'vue-slider-component';
export default {
  name: 'FilterBySquare',
  data(){
    return {
      menuText: 'Amaliegade 11A, 1.',
      minValue: 120,
      maxValue: 260,
      value: [
        120,
        220
      ],
      options: {
          width: "100%",
          height: 3,
          dotSize: 16,
          min: 120,
          max: 260,
          disabled: false,
          show: true,
          tooltip: "false",
          bgStyle: {
            "backgroundColor": "#fff",
            "boxShadow": "inset 0.5px 0.5px 3px 1px rgba(0,0,0,.36)"
          },
          tooltipStyle: {
            "backgroundColor": "#666",
            "borderColor": "#666"
          },
          processStyle: {
            "backgroundColor": "#ae252a"
        }
      }
    }
  },
  components: {
    vueSlider
  },
  methods: {
    handleChange(e) {
      this.menuText = e.target.firstChild.data;
    }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;

    .filterBySquare{
        margin: 0;
        .heading{
            text-align: left;
            font-weight: bold;
            .subtitle{
              margin-left: 10px;
              font-weight: normal;
              opacity: 0.5;
            }
        }

        .minPrice{
          float: left;
        }
        .maxPrice{
          float: right;
        }
    }

    .dropdown {
      .btn.dropdown-toggle{
        width: 100%;
        background-color: white;
        border: 1px solid #e6e6e6;
      }
    }


</style>
