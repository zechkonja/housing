<template>
  <div class="main " v-bind:class="{ 'col-sm-8': hideMain, 'col-sm-12': !hideMain}">
    <div class="heading">
      <div v-bind:class="{ hidden: hideMain, 'btnShowHide': !hideMain  }" @click="showHide"><i class="material-icons">sort</i> Filtering</div>
      <h5>Resultater</h5>
      <span>83 boliger</span>

      <div class="right-button-sorting">
        <button class="button-type current" @click="setCurrent($event)">Liste</button>
        <button class="button-type" @click="setCurrent($event)">Kort</button>
      </div>
    </div>
    <div class="sort">

      <div class="dropdown">
        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          {{menuText}}
        </button>
        <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
          <a class="dropdown-item" @click="handleChange" href="#">Newest</a>
          <a class="dropdown-item" @click="handleChange" href="#">Oldest</a>
        </div>
      </div>

    </div>

    <div class="houses">
      <AllHouses />
    </div>

  </div>
</template>

<script>
import AllHouses from '../components/AllHouses'
export default {
  name: 'Main',
  components: {
    AllHouses
  },
  props: {
     hideMain: {
       type: Boolean,
     }
  },
  data(){
    return {
      isHidden: true,
      menuText: 'Nyeste overst'
    }
  },
  methods: {
    showHide: function(){
      this.isHidden = true;
      this.$emit('update', this.isHidden);
    },
    setCurrent: function(event){
      let element = event.target;
      this.removeCurrentSiblings(element);
      element.classList.add('current');
    },
    removeCurrentSiblings: function (elem) {
        var siblings = [];
        var sibling = elem.parentNode.firstChild;
        var skipMe = elem;
        for ( ; sibling; sibling = sibling.nextSibling )
           if ( sibling.nodeType == 1 && sibling != elem ){
              sibling.classList.remove('current');
              siblings.push( sibling );
            }
        return siblings;
    },
    handleChange(e) {
      this.menuText = e.target.firstChild.data;
    }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;
  .hidden{
    display:none;
  }

  .main{
    .btnShowHide {
      display: inline-block;
      margin-right: 10px;
    }
    .heading{
      text-align: left;
      border-bottom: 1px solid #e6e6e6;
      padding-top: 15px;
      padding-bottom: 15px;
      h5 {
        display: inline-block;
      }
      span {
        display: inline-block;
      }

      .right-button-sorting{
        min-width: 200px;
        float: right;

        .button-type{
          width: 49%;
          display: inline-block;
          background-color: white;
          border: solid 1px #ccc;
          margin-bottom: 5px;
          padding-top: 3px;
          padding-bottom: 3px;
          opacity: 0.9;
          font-size: 14px;
        }

        .button-type.current{
          background-color: $main-bg-color;
          color: white;
        }
      }
    }

    .sort{
      text-align: right;
      margin-top: 15px;
      margin-bottom: 15px;

      .dropdown {
        .btn.dropdown-toggle{
          width: auto;
          background-color: white;
          border: solid 1px #ccc;
          border-radius: 0;
        }
      }
    }


  }

</style>
