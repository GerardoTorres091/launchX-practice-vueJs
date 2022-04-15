<template>
  <div class="container">
    <b-form @submit="onSubmit" @reset="onReset">
      <b-form-group id="input-group-2" label="Tu nombre:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          placeholder="Nombre"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-1"
        label="Tu correo electrónico:"
        label-for="input-1"
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          placeholder="Enter email"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Tu teléfono:" label-for="input-2">
        <b-form-input
          id="input-tel"
          v-model="form.phone"
          placeholder="Teléfono"
          type="number"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-4"
        label="Selecciona el pastel:"
        label-for="input-3"
      >
        <b-form-select
          id="input-3"
          v-model="form.cake"
          :options="cakes"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group
        v-if="showIfIsAMedida"
        id="input-group-5"
        label="Descibre lo mejor posible el pastel:"
        label-for="input-desc-cake"
      >
        <b-form-textarea
          id="input-desc-cake"
          v-model="form.descCake"
          placeholder="Descripción"
          rows="2"
          max-rows="4"
        ></b-form-textarea>
      </b-form-group>

      <b-form-group
        id="input-group-6"
        label="Selecciona el tamaño:"
        label-for="input-size"
      >
        <b-form-select
          id="input-ornament"
          v-model="form.size"
          :options="sizes"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group
        id="input-group-7"
        label="Selecciona el adorno:"
        label-for="input-ornament"
      >
        <b-form-select
          id="input-ornament"
          v-model="form.ornament"
          :options="ornaments"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group
        v-if="showIfIsFondant"
        id="input-group-8"
        label="Descibre lo mejor posible el tipo de adorno, puedes insertar imagen:"
        label-for="input-desc-fondant"
      >
        <b-form-textarea
          id="input-desc-fondant"
          v-model="form.descFondant"
          placeholder="Descripción"
          rows="2"
          max-rows="4"
        ></b-form-textarea>

      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>

    </b-form>

    <b-card class="mt-3" header="Datos que deben ser enviados a backend para guardar">
      <pre class="m-0">{{ form }}</pre>
      <pre>TODO: guardar imagenes, agregar validaciones en campos</pre>
    </b-card>

  </div>
</template>

<script>
export default {
  name: "showOrderForm",
  components: {},
  props: {id:{
      type: Number,
      default: null
  }},
  data: function () {
    return {
      form: {
        email: "",
        name: "",
        phone: null,
        cake: null,
        size: null,
        ornament: null,
        descCake: null,
        descFondant: null,
      },
      cakes: [
        { text: "Selecciona uno", value: null },
        "Coco-piña",
        "Choco naranja",
        "Vainilla chocolate",
        "Cajeta 3 leches",
        "A medida",
      ],
      ornaments: [
        { text: "Selecciona uno", value: null },
        "Tradicional merengue",
        "Chantilly",
        "Fondant, tu diseño favorito",
      ],
      sizes: [
        { text: "Selecciona uno", value: null },
        "1kg",
        "1/2kg",
        "1/4kg",
      ],
      show: true,
    };
  },
  mounted() {},
  computed: {
    //only if it is custom, show the text box for a better description
    showIfIsAMedida() {
      if (this.form.cake == "A medida") {
        return true;
      } else {
        return false;
      }
    },
    showIfIsFondant() {
      if (this.form.ornament == "Fondant, tu diseño favorito") {
        return true;
      } else {
        return false;
      }
    },
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(event) {
      event.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.cake = null;
      this.form.checked = [];
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    },
  },
  watch: {
        id:function(newVal){
            if(newVal){
                if(newVal == 1){
                    this.form.cake = 'Coco-piña';
                }else if(newVal == 2){
                    this.form.cake = 'Choco naranja';
                }else if(newVal == 3){
                    this.form.cake = 'Vainilla chocolate';
                }else if(newVal == 4){
                    this.form.cake = 'Cajeta 3 leches';
                }else if(newVal == 5){
                    this.form.cake = 'A medida';
                }
            }
        }
    }
};
</script>