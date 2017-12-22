
<template>
  <div class="filterByRequirement col-sm-12">
    <div class="heading">Bopælspligt</div>
    <button class="button-type" @click="setCurrent($event)">Ja</button>
    <button class="button-type" @click="setCurrent($event)">Nej</button>
  </div>
</template>

<script>
export default {
  name: 'FilterByRequirement',
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
    }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
$main-bg-color: #ae252a;
    .filterByRequirement{
        text-align: left;
        margin: 0;
        .heading{
            text-align: left;
            font-weight: bold;
        }

        .button-type{
          width: 20%;
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


</style>
