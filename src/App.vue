
<template>
  <div id="app">
    <SalutationName
      v-model:salutation="form.salutation"
      v-model:name="form.name"
    />
    <pre>{{ form }}</pre>
  </div>
</template>

<script>
import { reactive } from 'vue'
import SalutationName from './components/SalutationName'

export default {
  name: 'App',
  components: {
    SalutationName
  },
  setup () {
    const form = reactive({
      salutation: '',
      name: ''
    })

    return {
      form
    }
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
