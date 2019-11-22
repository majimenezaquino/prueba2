<template>
    <div>
  <b-card
    no-body
    style="max-width: 20rem;"
    img-src="https://placekitten.com/380/200"
    img-alt="Image"
    img-top
  >
    <template v-slot:header>
      <h4 class="mb-0">Hello World</h4>
    </template>

    <b-card-body>
     
      <b-card-sub-title class="mb-2">Card Sub Title</b-card-sub-title>
      <b-card-text>
        Some quick example text to build on the card title and make up the bulk of the card's
        content.
      </b-card-text>
    </b-card-body>

    

    <b-card-body>

      <a href="#" class="card-link">categoria</a>
    </b-card-body>

    <b-card-footer>This is a footer
      <b-button variant="warning" size="sm" class="mr-2">Edict</b-button>
      <b-button variant="danger" size="sm">Delete</b-button>
    </b-card-footer>

  
  </b-card>
</div>
</template>