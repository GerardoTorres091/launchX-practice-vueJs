<template>
    <div>
        <div class="text-center mt-5">
          <h2>Adornos</h2>
      </div>
      <b-card-group deck class="my-3">
        <b-card 
          title="Tradicional merengue"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>1kg    ... gratis</p>
            <p>1/2kg  ... gratis</p>
            <p>1/4kg  ... gratis</p>
          </b-card-text>
        </b-card>

        <b-card 
          title="Chantilly"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>1kg    ... + $100</p>
            <p>1/2kg  ... + $50</p>
            <p>1/4kg  ... + $40</p>
          </b-card-text>
        </b-card>

        <b-card 
          title="Fondant, tu diseño favorito"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>Recibimos tu diseño</p>
            <p>*el precio dependerá del diseño</p>
          </b-card-text>
        </b-card>
      </b-card-group>
    </div>
</template>

<script>

export default {
  name: "TypesOfOrnaments",
  components: {},
  props:{},
    data:function(){
        return {

        }
    },
    mounted(){

    },
    methods:{
    }
};
</script>