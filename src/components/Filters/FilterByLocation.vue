<template>
  <div class="filterByLocation col-sm-12">
    <div class="heading">Sog et sted</div>
    <div class="dropdown">
      <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        {{menuText}}
      </button>
      <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
        <a class="dropdown-item" @click="handleChange" href="#">Amaliegade 11A, 1.</a>
        <a class="dropdown-item" @click="handleChange" href="#">Dagmarsgade 17, 4.sal, 509</a>
        <a class="dropdown-item" @click="handleChange" href="#">Platanvej 7, 10.sal lejl. 46</a>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: 'FilterByLocation',
  data(){
    return {
      menuText: 'Amaliegade 11A, 1.'
    }
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

    .filterByLocation{
        margin: 0;
        .heading{
            text-align: left;
            font-weight: bold;
        }
    }

    .dropdown {
      .btn.dropdown-toggle{
        width: 100%;
        background-color: white;
        border: solid 1px #ccc;
        border-radius: 0;
      }
    }


</style>
