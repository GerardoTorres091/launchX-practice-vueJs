<template>
  <div>
    <b-jumbotron
      header="Nuestros Pasteles"
    >
    </b-jumbotron>

    <div class="container">
      
      <!--component that shows the available cakes-->
      <types-cakes></types-cakes>
      
      <!--component that shows the types of decorations that a cake can have-->
      <types-ornament></types-ornament>
      
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import TypesOfCakes from '@/components/TypesOfCakes.vue'
import TypesOfOrnaments from '@/components/TypesOfOrnaments.vue'

export default {
  name: "MenuPasteles",
  components: {
    'types-cakes'   : TypesOfCakes,
    'types-ornament' : TypesOfOrnaments
    },
  props:{},
    data:function(){
        return {

        }
    },
    mounted(){

    },
    methods:{
        sendPedido(id){
            alert('realizarás pedido'+id);
        }
    }
};
</script>