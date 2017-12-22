<template>
  <div class="col-sm-12 footer">
    <div class="row footer-row">
      <div class="col-sm-4 contact-logo">
        <a class="navbar-brand logo" href="#"><img src="../assets/images/logo.png" class="img-fluid" /></a>

        <h5>Sprog</h5>

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

        <h5>Tilmelde dig vores mailingliste</h5>

        <form class="form-inline search-mail">
          <div class="form-group">
            <label for="inputPassword2" class="sr-only">Password</label>
            <input type="text" class="form-control" id="inputPassword2" placeholder="">
          </div>
          <button type="submit" class="btn btn-primary findbyCaseNumber">Send</button>
        </form>

      </div>
      <div class="col-sm-8">
      <div class="row">
        <div class="col-sm-12">
          <div class="row">
            <div class="col-sm-3 rent">
              <div class="part">
                <h5>Udlej</h5>
                <p>Udlej bolig</p>
                <p>Boligberegner</p>
              </div>
            </div>
            <div class="col-sm-3 help">
              <div class="part">
                <h5>Hjaelp</h5>
                <p>Godt at vide</p>
                <p>Lejer</p>
                <p>Udlejer</p>
                <p>Okonomi</p>
              </div>
            </div>
            <div class="col-sm-3 about-us">
              <div class="part">
                <h5>Om os</h5>
                <p>Om Housing Denmark</p>
                <p>Organisationen</p>
                <p>team Housing Denmark</p>
                <p>Gor Karierre Hos Os</p>
                <p>Nyheder</p>
              </div>
            </div>
            <div class="col-sm-3 rental">
              <div class="part">
                <h5>Lejeboliger</h5>
                <p>Find boliger</p>
                <p>Opret konto</p>
                <p>Hotellejligheder</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-12">
          <div class="row">
          <div class="col-sm-3 rent">
            <div class="part">
              <h5>Folg os</h5>
              <p>Youtube</p>
              <p>Facebook</p>
              <p>Linkedin</p>
            </div>
          </div>
          <div class="col-sm-3 help">

            <div class="part">
              <h5>Vi stotter</h5>
              <p>img1</p>
              <p>img2</p>
            </div>
          </div>
          <div class="col-sm-3 about-us">

            <div class="part">
              <h5>Priser</h5>
              <p>img1</p>
              <p>img2</p>
              <p>img3</p>
            </div>
          </div>
          <div class="col-sm-3 rental">
            <div class="part">
            </div>
          </div>
        </div>
        </div>
      </div>
    </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Footer',
  data(){
    return {
      menuText: 'Dansk'
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
$main-bg-color: #ae252a;

   .footer .footer-row{
     margin-top: 50px;
     margin-bottom: 50px;
   }


   .contact-logo, .rent, .help, .about-us, .rental {
     text-align: left;
      margin-top: 10px;
      margin-bottom: 10px;
      color:white;
      font-size: 12px;
      h5{
        font-size: 14px;
        margin-bottom: 20px;
      }
      p{
        margin-bottom: 5px;
        color: #999999;
      }
      .part{

      }
   }

   .contact-logo{
     .logo{
       margin-bottom: 30px;
     }
   }

   .dropdown {
     margin-bottom: 25px;
     .btn.dropdown-toggle{
       color:white;
       width: 50%;
       background-color: #263138;
       border: solid 1px #263138;
       border-radius: 0;
     }
   }

   .search-mail{

   }

   .search-mail{
     input{
       border-radius: 0;
       background-color: #263138;
       border: solid 1px #263138;
     }
     .findbyCaseNumber {
       background-color: #1d262b;
       border: solid 1px #1d262b;
       color: white;
       box-shadow: none;
       border-radius: 0;
       cursor: pointer;
     }

   }


</style>
