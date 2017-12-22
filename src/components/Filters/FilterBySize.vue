<template>
  <div class="filterBySize col-sm-12">
    <div class="heading">Storrelse</div>
    <div class="dropdown">
      <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        {{menuText1}}
      </button>
      <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
        <a class="dropdown-item" @click="handleChange1" href="#">1 vaerelse</a>
        <a class="dropdown-item" @click="handleChange1" href="#">2 vaerelse</a>
        <a class="dropdown-item" @click="handleChange1" href="#">3 vaerelse</a>
        <a class="dropdown-item" @click="handleChange1" href="#">4 vaerelse</a>
        <a class="dropdown-item" @click="handleChange1" href="#">5+ vaerelse</a>
      </div>
    </div>
    <div class="dropdown">
      <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        {{menuText2}}
      </button>
      <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
        <a class="dropdown-item" @click="handleChange2" href="#">1 badevaerelse</a>
        <a class="dropdown-item" @click="handleChange2" href="#">2 badevaerelse</a>
        <a class="dropdown-item" @click="handleChange2" href="#">3 badevaerelse</a>
        <a class="dropdown-item" @click="handleChange2" href="#">4 badevaerelse</a>
        <a class="dropdown-item" @click="handleChange2" href="#">5+ badevaerelse</a>
      </div>
    </div>
    <div class="dropdown">
      <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
        {{menuText3}}
      </button>
      <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
        <a class="dropdown-item" @click="handleChange3" href="#">1 stuer</a>
        <a class="dropdown-item" @click="handleChange3" href="#">2 stuer</a>
        <a class="dropdown-item" @click="handleChange3" href="#">3 stuer</a>
        <a class="dropdown-item" @click="handleChange3" href="#">4 stuer</a>
        <a class="dropdown-item" @click="handleChange3" href="#">5+ stuer</a>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'FilterBySize',
  data(){
    return {
      menuText1: 'Vaerelser',
      menuText2: 'Badevaerelser',
      menuText3: 'Stuer',
    }
  },
  methods: {
    handleChange1(e) {
      this.menuText1 = e.target.firstChild.data;
    },
    handleChange2(e) {
      this.menuText2 = e.target.firstChild.data;
    },
    handleChange3(e) {
      this.menuText3 = e.target.firstChild.data;
    },
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;

    .filterBySize{
        margin: 0;
        .heading{
            text-align: left;
            font-weight: bold;
        }

        .dropdown {
          display: inline-block;
          float: left;
          margin-bottom: 5px;
          margin-right: 5px;
          .btn.dropdown-toggle{
            width: 100%;
            background-color: white;
            border: solid 1px #ccc;
            border-radius: 0;
          }
        }


    }


</style>
