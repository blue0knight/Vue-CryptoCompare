<template>
   <div class="container">
      <h3 class="text-center">BTC vs ETH</h3>
      <div class="row bg-light">
      
        <div class="columns col-md-6" v-for="(result, index) in results">
          <div class="card-body text-center">
            <div class="card-section">
              <p> {{ index }} </p>
            </div>
            <div class="card-text">
              <p>$ {{ result.USD }}</p>
            </div>
            <div class="card-text">
              <p>&#8364 {{ result.EUR }}</p>
            </div>

          </div>
        </div>

      </div> 
    </div>
</template>


<script>
const url = "https://min-api.cryptocompare.com/data/pricemulti?fsyms=BTC,ETH&tsyms=USD,EUR";
import axios from 'axios'

export default {
  name: 'crypto',
  data: () => ({
    results: [],
    errors: []
  }),

    mounted() {
      axios.get(url).then(response => {
        this.results = response.data
      })
        
    .catch(e => {
      this.errors.push(e)
    })
  },

}              
     

</script>

