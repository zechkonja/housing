<template>
  <div class="allhouses">
    <div class="row">
    <div v-for="house in houses" class="col-sm-6 house">
      <div class="header-image">
        <img v-bind:src='house.featured_image_url' class="img-fluid" />
      </div>
      <div class="title">
        <h4>{{house.localized_title}}</h4>
      </div>
      <div class="details">
        <div class="address">
          {{house.name}}, {{house.post_code}}
        </div>
        <span>No. {{house.case_number}}</span>
      </div>
      <div class="short-desc">
        {{house.localized_short_description}}
      </div>
      <div class="house-detail">
        <span>{{house.surface_area}} m2</span> - <span> {{house.rent_amount}} DKK/ md.</span>
      </div>
    </div>
    <div class="col-sm-12">
      <button class="load-more">indlæser...</button>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  name: 'AllHouses',
  data(){
    return {
      houses: [
        {
          featured_image_url: "src/assets/images/house1.jpg",
          localized_title: "Kajelberg Villa",
          name: "Frederiksberg",
          post_code:2000,
          case_number:29364463,
          localized_short_description:"Neque porro quisquam est qui dolorem iectetur",
          rent_amount:20000,
          surface_area:150
        },
        {
          featured_image_url: "src/assets/images/house2.jpg",
          localized_title: "New York Villa",
          name: "Hellerup",
          post_code:2100,
          case_number:29377463,
          localized_short_description:"Neque porro quisquam est qui dolorem ipsum quia dolor sit amet",
          rent_amount:45000,
          surface_area:450
        },
        {
          featured_image_url: "src/assets/images/house3.jpg",
          localized_title: "Nice Villa",
          name: "Kongens Lyngby",
          post_code:2090,
          case_number:23364463,
          localized_short_description:"Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur",
          rent_amount:29000,
          surface_area:290
        },
      ]

    }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

  .house{
    margin-bottom: 40px;
    text-align: left;

    .header-image{
      margin-bottom: 20px;
    }


    .details {
      margin-bottom: 15px;
      div {
        display: inline-block;
      }
      span {
        font-size: 14px;
        float: right;
      }
    }

    .short-desc{
      margin-bottom: 15px;
      font-size: 14px;
      opacity: 0.6;
    }

    .house-detail{
      font-size: 14px;
    }

  }

  .load-more{
      width: 50%;
      display: inline-block;
      background-color: white;
      border: none;
      margin-bottom: 5px;
      padding-top: 3px;
      padding-bottom: 3px;
      opacity: 0.5;
      font-size: 12px;
      &:hover{
        cursor: pointer;
      }
  }


</style>
