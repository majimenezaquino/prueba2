<template>
    <div>
       <div>
  

  <b-modal id="create_new_product_category" title="New Category" hide-footer>
    <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      <b-form-group
        id="input-group-1"
        label="Category Name"
        label-for="input-1"
      
      >
        <b-form-input
          v-model="form.email"
          type="text"
          required
        ></b-form-input>
      </b-form-group
      >
      
          <b-form-group
        id="input-group-1"
        label="Category Description"
        label-for="input-1"
      
      >
        <b-form-input
          v-model="form.email"
          type="text"
          required
        ></b-form-input>
      </b-form-group
      >
      


     


      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset" variant="danger">Reset</b-button>
    </b-form>
   
  </div>
  </b-modal>
</div> 
    </div>
</template>
<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          name: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.name = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    }
  }
</script>