<template>
  <div class="topNav">
    <ul>
      <li><div><a class="active" href="#">Premium</a></div></li>
      <li><div><a href="#">Marketplace</a></div></li>
      <li><div><a href="#">Services</a></div></li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'TopNav',
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;
.topNav{
  background-color: #f7f7f7;
  text-align: left;
  position: relative;
  ul {
    padding-left: 0;
    margin-bottom: 0;
    font-size: 0;
    li {
      display: inline-block;
      a{
        display: block;
        font-size: 14px;
        color: #4a4a4a;
        padding: 6px 25px;
        text-decoration: none;
      }
      a:hover{
        background-color: $main-bg-color;
        color: white;
      }
      a.active{
        background-color: $main-bg-color;
        color: white;
      }
    }

  }


}


</style>
