<template>
  <div class="appContainer">
      <TopNav />
      <AppHeader />
  <div class="container">
      <div class="row">
          <Filters :hideFilters="hideFilters" @update="updateFilters" />
          <AppMain :hideMain="hideMain" @update="updateMain"/>
      </div>
  </div>
  <div class="contact-block">
    <div class="container">
      <div class="row">
        <ContactBlock />
      </div>
    </div>
  </div>
  <div class="footer">
    <div class="container">
      <div class="row">
        <AppFooter />
      </div>
    </div>
  </div>
</div>
</template>

<script>
import TopNav from '../components/TopNav'
import AppHeader from '../components/Header'
import Filters from '../components/Filters'
import AppMain from '../components/Main'
import ContactBlock from '../components/ContactBlock'
import AppFooter from '../components/Footer'


export default {
  name: 'Container',
  components: {
    TopNav, AppHeader, Filters, AppMain, ContactBlock, AppFooter
  },
  data(){
    return {
      hideFilters: (this.windowWidth < 768) ? true:false,
      hideMain: true
    }
  },
  methods: {
      updateFilters: function(v){
        this.hideFilters = v;
        this.hideMain = false;
      },
      updateMain: function(v){
        this.hideMain = v;
        this.hideFilters = false;
      },
      getWindowWidth: function(event) {
  				return document.documentElement.clientWidth;
  		},
  },
  mounted() {
		this.$nextTick(function() {
				window.addEventListener('resize', this.getWindowWidth());
		})

    if(this.windowWidth < 768){
      this.hideFilters = true;
      this.hideMain = false;
    } else {
      this.hideFilters = false;
      this.hideMain = true;
    }
	},
	computed: {
		windowWidth() {
				return this.getWindowWidth();
		}
	}
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  @font-face {
      font-family: MyriadPro;
      src: url("../assets/fonts/MyriadPro-Regular.otf") format("opentype");
  }

  .container {
      max-width: 1400px;
      width: 90%;
      margin-top: 47px;
    }

  .contact-block{
    background-color: #fbfbfd;
  }

  .footer{
    background-color: #151b1f;
  }

  .footer .container{
    margin-top: 0;
  }

</style>
