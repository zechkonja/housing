<template>
  <div class="header">
        <nav class="navbar navbar-expand-lg navbar-light">
          <a class="navbar-brand" href="#"><img src="../assets/images/logo.png" class="img-fluid" /></a>
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
            </ul>
            <ul class="navbar-nav ml-auto">
              <li class="nav-item">
                <a class="nav-link" href="#">Find boliger <span class="sr-only">(current)</span></a>
              </li>
              <li class="navbar-item">
                <a class="nav-link" href="#">Udlej boliger</a>
              </li>
              <li class="navbar-item">
                <a class="nav-link" href="#">Help</a>
              </li>
            </ul>
          </div>
          <form class="form-inline my-2 my-lg-0">
            <input class="form-control mr-sm-2" type="search" placeholder="Log ind" aria-label="Log ind">
            <button class="btn search-btn" type="submit"><i class="material-icons">search</i></button>
          </form>
        </nav>
  </div>
</template>

<script>

export default {
  name: 'Header',
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;
 .header {
    border-bottom: 1px solid #e6e6e6;
    nav{
      margin-left: 30px;
      margin-right: 30px;
    }
    .search-btn{
      background-color: white;
      display: inline-flex;
    }
    .navbar-toggler{
      border: 0;
    }
 }

 input {
  	outline: none;
  }
  input[type=search] {
  	-webkit-appearance: textfield;
  	-webkit-box-sizing: content-box;
  	font-family: inherit;
  	font-size: 100%;
  }
  input::-webkit-search-decoration,
  input::-webkit-search-cancel-button {
  	display: none;
  }


  input[type=search] {
  	border: solid 1px #ccc;
  	padding: 9px 20px 9px 20px;
  	width: 55px;

  	-webkit-border-radius: 10em;
  	-moz-border-radius: 10em;
  	border-radius: 10em;

  	-webkit-transition: all .5s;
  	-moz-transition: all .5s;
  	transition: all .5s;
  }
  input[type=search]:focus {
  	width: 130px;
  	background-color: #fff;
  	border-color: #ccc;

  	-webkit-box-shadow: 0 0 5px rgba(109,207,246,.5);
  	-moz-box-shadow: 0 0 5px rgba(109,207,246,.5);
  	box-shadow: 0 0 5px rgba(109,207,246,.5);
  }


  input:-moz-placeholder {
  	color: #999;
  }
  input::-webkit-input-placeholder {
  	color: #999;
  }


// Extra small devices (portrait phones, less than 576px)
@media (max-width: 575px) {
  .header {
     nav{
       margin-left: 0px;
       margin-right: 0px;
     }
   }
}

// Small devices (landscape phones, less than 768px)
@media (max-width: 767px) {  }

// Medium devices (tablets, less than 992px)
@media (max-width: 991px) {  }

// Large devices (desktops, less than 1200px)
@media (max-width: 1199px) {  }

</style>
