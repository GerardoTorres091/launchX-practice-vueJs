<template>
  <div>
    <b-jumbotron
      header="Realizar pedido"
    >
    </b-jumbotron>

    <order-form :id="id"></order-form>
    

  </div>
</template>

<script>
// @ is an alias to /src
import showOrderForm from '@/components/showOrderForm.vue'

export default {
  name: "OrderForm",
  components: {
      'order-form' : showOrderForm,
  },
  props:{},
    data:function(){
        return {
            id:null,
        }
    },
    mounted(){
        this.id = this.$route.params.id;
    },
    methods:{
    },
    watch: {
    }
};
</script>