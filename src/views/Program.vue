<template>
  <div class="Program">
    <img alt="Vue logo" src="../assets/logo.png">
    <ProgramApi results="Welcome program apie view"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ProgramApi from '@/components/ProgramApi.vue'

export default {
  name: 'Program',
  components: {
    ProgramApi
  }
}
</script>
