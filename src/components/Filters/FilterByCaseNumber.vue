
<template>
  <div class="filterByCaseNumber col-sm-12">
    <div class="heading">Søg efter sagsnummer</div>
    <div class="search-form">
      <form class="form-inline">
        <div class="form-group">
          <label for="inputPassword2" class="sr-only">Password</label>
          <input type="text" class="form-control" id="inputPassword2" placeholder="">
        </div>
        <button type="submit" class="btn btn-primary findbyCaseNumber">Sok</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FilterByCaseNumber',
  data(){
    return {
      isActive: false,
      date: new Date(),
      config: {
          format: 'DD/MM/YYYY',
      }
    }
  },
  methods: {
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;
    .filterByCaseNumber{
        text-align: left;
        margin: 0;
        .heading{
            text-align: left;
            font-weight: bold;
        }

        .search-form{
          input{
            border-radius: 0;
          }
          .findbyCaseNumber {
            margin-left: 10px;
            background-color: white;
            box-shadow: none;
            border: solid 1px #ccc;
            border-radius: 0;
            color: black;
            cursor: pointer;
          }

        }
    }



</style>
