<template>
  <v-container fluid grid-list-lg style="margin-bottom: 1.5em">
    <v-layout row wrap>
      
      <v-flex xs12>
        <v-card color="blue-grey darken-2" class="white--text">
          <v-card-title primary-title>
            <div class="headline">Air</div>
          </v-card-title>
          <v-card-actions>
            <v-btn dark color="orange">Book now</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      
      <v-flex xs12>
        <v-card color="cyan darken-2" class="white--text">
          <v-card-title primary-title>
            <div class="headline">Hotel</div>
          </v-card-title>
          <v-card-actions>
            <v-btn color="orange" dark>Book now</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      
      
      <v-flex xs12>
        <v-card color="purple darken-2" class="white--text">
          <v-card-title primary-title>
            <div class="headline">Car</div>
          </v-card-title>
          <v-card-actions>
            <v-btn color="orange" dark>Book now</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    
    </v-layout>
  </v-container>
</template>
<script>
  export default {
    name: 'home',
    components: {}
  }
</script>
