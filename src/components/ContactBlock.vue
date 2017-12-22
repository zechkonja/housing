<template>
  <div class="col-sm-12 contactBlock">
    <div class="row">
      <div class="col-sm-4 blog">
        <h4>Nyheder</h4>
        <div class="blog-post">
          <h5>Blog post title here</h5>
          <span>12. September 2016.</span>
          <div class="blog-text">
            Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit
          </div>
        </div>
        <div class="blog-post">
          <h5>Blog post title here</h5>
          <span>12. September 2016.</span>
          <div class="blog-text">
            Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit
          </div>
        </div>

      </div>
      <div class="col-sm-2">
      </div>
      <div class="col-sm-6 contact">
        <div class="row">
          <div class="col-sm-6">
            <div class="contact-us">
              <h4>Kontakt os</h4>
              <div>
                Neque porro quisquam est qui dolorem ipsum, st qui dolorem ipsum st qui dolorem
              </div>
            </div>
            <div class="telephone">
              <h4>Ring os pa telefon</h4>
              <div>
                +45 70 2004 70
              </div>
            </div>
            <span class="trine">Kontakt Trine</span>
        </div>
        <div class="col-sm-6 contact-image">
          <img src="../assets/images/contactPerson.png" class="img-fluid" />
        </div>
      </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'ContactBlock',
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;
   .contactBlock{
     margin: auto;
   }

   .blog{
     margin-top: 50px;
     text-align: left;
     h4 {
       font-size: 18px;
       margin-bottom: 20px
     }
     .blog-post{
       margin-bottom: 20px;
       h5{
         font-weight: bold;
         margin-bottom: 0;
       }
       span{
         margin-top: 10px;
         font-size: 12px;
         opacity: 0.6;
       }
       .blog-text{
         font-size: 12px;
         opacity: 0.6;
         margin-top: 7px;
       }
     }
   }

   .contact{
     margin-top: 50px;
     text-align: left;
     .contact-us, .telephone{
       margin-bottom: 15px;
       h4{
         font-size: 18px;
         margin-bottom: 10px
       }
       div {
         font-size: 12px;
         opacity: 0.6;
       }
     }
     .trine{
       color: $main-bg-color;
       font-size: 12px;
       font-weight: bold;
     }

   }

   .contact-image{
   }

</style>
