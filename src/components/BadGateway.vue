<template>
  <section id="bad-gateway">
    <div class="full">
      <row class="bad-gateway-row">
        <column md="8">
          <img alt="Error 404" class="img-fluid" hieght="20px" src="../assets/logo-mdb-vue-small.png"/>
          <h2 class="h2-responsive mt-3 mb-2">404. That's an error.</h2>
          <h4>The requested URL was not found on this server.</h4>
        </column>
        <column md="4">
          <img alt="Error 404" class="img-fluid" src="https://mdbootstrap.com/img/Others/grafika404-bf.png"/>
        </column>
      </row>
    </div>
  </section>
</template>

<script>
import { Row, Column } from 'mdbvue'

export default {
  name: 'BadGateway',
  components: {
    Row,
    Column
  },
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.full {
  height: 70vh;
}
.bad-gateway-row {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 55%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}
</style>
