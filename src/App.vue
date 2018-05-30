<template>
  <div class="flexible-content">
    <!--Navbar-->
    <navbar class="flexible-navbar white" position="top" name="MDB" href="#" scrolling>
      <navbar-collapse>
        <navbar-nav left>
          <router-link to="/dashboard" @click.native="activeItem = 1"><navbar-item href="" waves-fixed active>Home</navbar-item></router-link>
          <navbar-item href="https://mdbootstrap.com/vue/vue-bootstrap-getting-started/" waves-fixed>About MDB</navbar-item>
          <navbar-item href="https://mdbootstrap.com/vue/vue-bootstrap-getting-started/" waves-fixed>Free download</navbar-item>
          <navbar-item href="https://mdbootstrap.com/bootstrap-tutorial/" waves-fixed>Free tutorials</navbar-item>
        </navbar-nav>
        <navbar-nav right>
          <navbar-item href="#!" waves-fixed><fa class="text-black" icon="facebook"/></navbar-item>
          <navbar-item href="#!" waves-fixed><fa icon="twitter"/></navbar-item>
          <navbar-item href="https://github.com/mdbootstrap/bootstrap-material-design" waves-fixed class="border border-light rounded mr-1" target="_blank"><fa icon="github" class="mr-2"/>MDB GitHub </navbar-item>
          <navbar-item href="https://mdbootstrap.com/product/vue-bootstrap-pro/" waves-fixed class="border border-light rounded" target="_blank"><fa icon="diamond" class="mr-2"/>Go Pro </navbar-item>
        </navbar-nav>
      </navbar-collapse>
    </navbar>
    <!--/.Navbar-->
    <!-- Sidebar -->
    <div class="sidebar-fixed position-fixed">
      <a class="logo-wrapper"><img alt="" class="img-fluid" src="./assets/logo-mdb-vue-small.png"/></a>
      <list-group class="list-group-flush">
        <router-link to="/dashboard" @click.native="activeItem = 1">
          <list-group-item :action="true" :class="activeItem === 1 && 'active'"><fa icon="pie-chart" class="mr-3"/>Dashboard</list-group-item>
        </router-link>
        <router-link to="/profile" @click.native="activeItem = 2">
          <list-group-item :action="true" :class="activeItem === 2 && 'active'"><fa icon="user" class="mr-3"/>Profile</list-group-item>
        </router-link>
        <router-link to="/tables"  @click.native="activeItem = 3">
          <list-group-item :action="true" :class="activeItem === 3 && 'active'"><fa icon="table" class="mr-3"/>Tables</list-group-item>
        </router-link>
        <router-link to="/maps" @click.native="activeItem = 4">
          <list-group-item :action="true" :class="activeItem === 4 && 'active'"><fa icon="map" class="mr-3"/>Maps</list-group-item>
        </router-link>
        <router-link to="/404" @click.native="activeItem = 5">
          <list-group-item :action="true" :class="activeItem === 5 && 'active'"><fa icon="exclamation" class="mr-3"/>404</list-group-item>
        </router-link>
      </list-group>
    </div>
    <!-- /Sidebar  -->
    <main>
      <div class="mt-5 p-5">
        <router-view></router-view>
      </div>
      <ftr color="primary-color-dark" class="text-center font-small darken-2">
        <div class="pt-4">
          <btn outline="white" tag="a" href="https://mdbootstrap.com/getting-started/" target="_blank">Download MDB <fa icon="download" class="ml-2"/></btn>
          <btn outline="white" tag="a" href="https://mdbootstrap.com/bootstrap-tutorial/" target="_blank">Start free tutorial <fa icon="graduation-cap" class="ml-2"/></btn>
        </div>
        <hr class="my4"/>
        <div class="pb-4">
          <a href="#"><fa icon="facebook" class="mr-3"/></a>
          <a href="#"><fa icon="twitter" class="mr-3"/></a>
          <a href="#"><fa icon="youtube" class="mr-3"/></a>
          <a href="#"><fa icon="google-plus" class="mr-3"/></a>
          <a href="#"><fa icon="dribbble" class="mr-3"/></a>
          <a href="#"><fa icon="pinterest" class="mr-3"/></a>
          <a href="#"><fa icon="github" class="mr-3"/></a>
          <a href="#"><fa icon="codepen" class="mr-3"/></a>
        </div>
        <p class="footer-copyright mb-0 py-3 text-center">
          &copy; {{new Date().getFullYear()}} Copyright: <a href="https://www.MDBootstrap.com"> MDBootstrap.com </a>
        </p>
      </ftr>
    </main>
  </div>
</template>

<script>
import { Container, Navbar, NavbarItem, NavbarNav, NavbarCollapse, Btn, Fa, ListGroup, ListGroupItem, CardBody, Footer, waves } from 'mdbvue'
import Dashboard from './components/Dashboard'
import Profile from './components/Profile'

export default {
  name: 'AdminTemplate',
  components: {
    Container,
    Navbar,
    NavbarItem,
    NavbarNav,
    NavbarCollapse,
    Btn,
    ListGroup,
    ListGroupItem,
    Fa,
    CardBody,
    'ftr': Footer,
    Dashboard,
    Profile
  },
  data () {
    return {
      activeItem: 1
    }
  },
  beforeMount () {
    this.activeItem = this.$route.matched[0].props.default.page
  },
  mixins: [waves]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
main {
  background-color: #EDEDEE;
}

.flexible-content {
  transition: padding-left 0.3s;
  padding-left: 270px;
}

.flexible-navbar {
  transition: padding-left 0.5s;
  padding-left: 270px;
}

.sidebar-fixed {
  left: 0;
  top: 0;
  height: 100vh;
  width: 270px;
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
  z-index: 1050;
  background-color: #fff;
  padding: 1.5rem;
  padding-top: 0;
}

.sidebar-fixed .logo-wrapper img{
  width: 100%;
  padding: 2.5rem;
}

.sidebar-fixed .list-group-item {
  display: block !important;
  transition: background-color 0.3s;
}

.sidebar-fixed .list-group .active {
  box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);
  border-radius: 5px;
}

@media (max-width: 1199.98px) {
  .sidebar-fixed {
    display: none;
  }
  .flexible-content {
    padding-left: 0;
  }
  .flexible-navbar {
    padding-left: 10px;
  }
}
</style>
<style>
.navbar-light .navbar-brand {
  margin-left: 15px;
  color: #2196f3 !important;
  font-weight: bolder;
}
</style>
