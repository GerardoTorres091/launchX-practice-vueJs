<template>
  <div>
    <b-jumbotron
      header="Nuestros Pasteles"
    >
    </b-jumbotron>

    <div class="container">
      <b-card-group deck class="my-3">
        <b-card 
          title="Coco-piña"
          :img-src="require('../assets/pastel1.png')"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>1kg    ... $500</p>
            <p>1/2kg  ... $300</p>
            <p>1/4kg  ... $150</p>
          </b-card-text>
          <template #footer>
           <b-button pill variant="primary" @click="sendPedido(1)">Realizar pedido</b-button>
          </template>
        </b-card>

        <b-card 
          title="Choco naranja"
          :img-src="require('../assets/pastel1.png')"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>1kg    ... $500</p>
            <p>1/2kg  ... $300</p>
            <p>1/4kg  ... $150</p>
          </b-card-text>
          <template #footer>
            <b-button pill variant="primary" @click="sendPedido(2)">Realizar pedido</b-button>
          </template>
        </b-card>

        <b-card 
          title="Vainilla chocolate"
          :img-src="require('../assets/pastel1.png')"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>1kg    ... $500</p>
            <p>1/2kg  ... $300</p>
            <p>1/4kg  ... $150</p>
          </b-card-text>
          <template #footer>
            <b-button pill variant="primary" @click="sendPedido(3)">Realizar pedido</b-button>
          </template>
        </b-card>
      </b-card-group>


      <b-card-group deck>
        <b-card
          title="Cajeta 3 leches"
          :img-src="require('../assets/pastel1.png')"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>1kg    ... $500</p>
            <p>1/2kg  ... $300</p>
            <p>1/4kg  ... $150</p>
          </b-card-text>
          <template #footer>
            <b-button pill variant="primary" @click="sendPedido(4)">Realizar pedido</b-button>
          </template>
        </b-card>

        <b-card
          title="A medida"
          :img-src="require('../assets/pastel2.png')"
          img-alt="Image"
          img-top
        >
          <b-card-text>
            <p>Precios desde $300 hasta $800</p>
            <p>*depende modelo</p>
          </b-card-text>
          <template #footer>
            <b-button pill variant="primary" @click="sendPedido(5)">Realizar pedido</b-button>
          </template>
        </b-card>
      </b-card-group>
      
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

  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "MenuPasteles",
  components: {},
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