<template>
  <div class="filterByPrice col-sm-12">
    <div class="heading">Husleje <span class="subtitle">Maxpris (DKK)</span></div>
    <vue-slider v-model="value"  v-bind="options"></vue-slider>
    <span class="minPrice">{{minValue}}</span><span class="maxPrice">{{maxValue}}</span>
  </div>
</template>

<script>

import vueSlider from 'vue-slider-component';
export default {
  name: 'FilterByPrice',
  data(){
    return {
      menuText: 'Amaliegade 11A, 1.',
      minValue: 5000,
      maxValue: 15000,
      value: [
        5000,
        8000
      ],
      options: {
          width: "100%",
          height: 3,
          dotSize: 16,
          min: 5000,
          max: 15000,
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

    .filterByPrice{
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
