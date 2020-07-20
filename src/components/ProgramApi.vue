<template>
  <div class="program">
    <div class="container" id="app">
      <h3 class="text-center">Programs Api Connection using Vue</h3>
    <div class="columns medium-4" v-bind:key=result.id v-for="(result, index) in results" >
          <div class="card-section">
            <p> {{ index }} </p>
          </div>
          <div class="card-divider">
            <p> {{ result.id}} {{ result.name}} {{result.version}} {{result.description}}</p>
          </div>
        <div class="card-section">
        </div>
        
    </div>
    
    </div>
  </div>
</template>


<script>
import axios from 'axios';
export default {
  name: 'ProgramApi',
  props: {
    resultsname: String
  },
  data() {
    return {
      results: [],
    };
  },
  created: function() {
    axios.get('http://localhost:3001/api/getDataProgram')
    .then(response => {
      this.results = response.data.dataprogram;
    })
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
  color:blue;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
p {
  display: inline-block;
}
</style>
