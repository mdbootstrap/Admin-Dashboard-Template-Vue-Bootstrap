<template>
  <div class="hello">
    <h3>{{ msg }}</h3>
    <p class="mb-2">The application is configured and ready to import our components. You will find MDB Vue docs <a href="https://mdbootstrap.com/docs/vue/" target="_blank">here</a>.</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your MDB Vue.js App'
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  font-weight: normal;
  padding-top: 20px;
  padding-bottom: 30px;
}
p {
  color: #969696;
  margin-bottom: 0;
  font-size: 14px;
}
</style>
