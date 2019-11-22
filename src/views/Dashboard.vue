<template>
  <div class="home">
    
    <NavBard />
    <CreateProduct />
    <CreateProductCategory />
    <b-container>
      <template>
  <b-breadcrumb> 
    <b-breadcrumb-item> 
      <b-button variant="primary" @click="openModalNewProduct">New Product</b-button> 
      </b-breadcrumb-item>
    <b-breadcrumb-item> <b-button variant="primary" @click="openModalNewProductCategory"> New Category</b-button>  </b-breadcrumb-item>
   </b-breadcrumb>
</template>
<b-row>
    <b-col>
      <Product />
    </b-col>
  </b-row>
</b-container>
  </div>
</template>

<script>
// @ is an alias to /src

import NavBard from '@/components/navbard.vue'
import Product from '@/components/Products.vue'
import CreateProduct from '@/components/create-products.vue'
import CreateProductCategory from '@/components/create-products-category.vue'

export default {
  name: 'home',
  components: {
    NavBard,
    Product,
    CreateProduct,
    CreateProductCategory
  },
   data() {
      return {
        items: [
          {
            text: 'Admin',
            href: '#'
          },
          {
            text: 'Manage',
            href: '#'
          },
          {
            text: 'Library',
            active: true
          }
        ]
      }
    },
    methods:{
      openModalNewProduct(){
        this.$bvModal.show("create_new_product")
      },
      openModalNewProductCategory(){
        this.$bvModal.show("create_new_product_category")
      }
    }
}
</script>
