<template>
  <div class="flexible-content">
    <!--Navbar-->
    <mdb-navbar class="flexible-navbar white" light position="top" scrolling>
      <mdb-navbar-brand href="https://mdbootstrap.com/docs/vue/" target="_blank"
        >MDB</mdb-navbar-brand
      >
      <mdb-navbar-toggler>
        <mdb-navbar-nav left>
          <mdb-nav-item to="/" waves-fixed active class="active"
            >Home</mdb-nav-item
          >
          <mdb-nav-item
            href="https://mdbootstrap.com/docs/vue/getting-started/quick-start/"
            waves-fixed
            >About MDB</mdb-nav-item
          >
          <mdb-nav-item
            href="https://mdbootstrap.com/docs/vue/getting-started/download/"
            waves-fixed
            >Free download</mdb-nav-item
          >
          <mdb-nav-item
            href="https://mdbootstrap.com/education/bootstrap/"
            waves-fixed
            >Free tutorials</mdb-nav-item
          >
        </mdb-navbar-nav>
        <mdb-navbar-nav right>
          <mdb-nav-item href="#!" waves-fixed
            ><mdb-icon fab class="text-black" icon="facebook-square"
          /></mdb-nav-item>
          <mdb-nav-item href="#!" waves-fixed
            ><mdb-icon fab icon="twitter"
          /></mdb-nav-item>
          <mdb-nav-item
            href="https://github.com/mdbootstrap/bootstrap-material-design"
            waves-fixed
            class="border border-light rounded mr-1"
            target="_blank"
            ><mdb-icon fab icon="github" class="mr-2" />MDB GitHub
          </mdb-nav-item>
          <mdb-nav-item
            href="https://mdbootstrap.com/products/vue-ui-kit/"
            waves-fixed
            class="border border-light rounded"
            target="_blank"
            ><mdb-icon icon="gem" far class="mr-2" />Go Pro
          </mdb-nav-item>
        </mdb-navbar-nav>
      </mdb-navbar-toggler>
    </mdb-navbar>
    <!--/.Navbar-->
    <!-- Sidebar -->
    <div class="sidebar-fixed position-fixed">
      <a class="logo-wrapper"
        ><img alt="" class="img-fluid" src="./assets/logo-mdb-vue-small.png"
      /></a>
      <mdb-list-group class="list-group-flush">
        <router-link to="/dashboard" @click.native="activeItem = 1">
          <mdb-list-group-item
            :action="true"
            :class="activeItem === 1 && 'active'"
            ><mdb-icon
              icon="chart-pie"
              class="mr-3"
            />Dashboard</mdb-list-group-item
          >
        </router-link>
        <router-link to="/profile" @click.native="activeItem = 2">
          <mdb-list-group-item
            :action="true"
            :class="activeItem === 2 && 'active'"
            ><mdb-icon icon="user" class="mr-3" />Profile</mdb-list-group-item
          >
        </router-link>
        <router-link to="/tables" @click.native="activeItem = 3">
          <mdb-list-group-item
            :action="true"
            :class="activeItem === 3 && 'active'"
            ><mdb-icon icon="table" class="mr-3" />Tables</mdb-list-group-item
          >
        </router-link>
        <router-link to="/maps" @click.native="activeItem = 4">
          <mdb-list-group-item
            :action="true"
            :class="activeItem === 4 && 'active'"
            ><mdb-icon icon="map" class="mr-3" />Maps</mdb-list-group-item
          >
        </router-link>
        <router-link to="/404" @click.native="activeItem = 5">
          <mdb-list-group-item
            :action="true"
            :class="activeItem === 5 && 'active'"
            ><mdb-icon
              icon="exclamation"
              class="mr-3"
            />404</mdb-list-group-item
          >
        </router-link>
      </mdb-list-group>
    </div>
    <!-- /Sidebar  -->
    <main>
      <div class="mt-5 p-5">
        <router-view></router-view>
      </div>
      <ftr color="primary-color-dark" class="text-center font-small darken-2">
        <div class="pt-4">
          <mdb-btn
            outline="white"
            tag="a"
            href="https://mdbootstrap.com/docs/vue/getting-started/download/"
            target="_blank"
            >Download MDB <mdb-icon icon="download" class="ml-2"
          /></mdb-btn>
          <mdb-btn
            outline="white"
            tag="a"
            href="https://mdbootstrap.com/education/bootstrap/"
            target="_blank"
            >Start free tutorial <mdb-icon icon="graduation-cap" class="ml-2"
          /></mdb-btn>
        </div>
        <hr class="my4" />
        <div class="pb-4">
          <a href="#"><mdb-icon fab icon="facebook-square" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="twitter" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="youtube" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="google-plus" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="dribbble" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="pinterest" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="github" class="mr-3"/></a>
          <a href="#"><mdb-icon fab icon="codepen" class="mr-3"/></a>
        </div>
        <p class="footer-copyright mb-0 py-3 text-center">
          &copy; {{ new Date().getFullYear() }} Copyright:
          <a href="https://mdbootstrap.com/docs/vue/"> MDBootstrap.com </a>
        </p>
      </ftr>
    </main>
  </div>
</template>

<script>
import {
  mdbNavbar,
  mdbNavbarBrand,
  mdbNavItem,
  mdbNavbarNav,
  mdbNavbarToggler,
  mdbBtn,
  mdbIcon,
  mdbListGroup,
  mdbListGroupItem,
  mdbFooter,
  waves
} from "mdbvue";

export default {
  name: "AdminTemplate",
  components: {
    mdbNavbar,
    mdbNavbarBrand,
    mdbNavItem,
    mdbNavbarNav,
    mdbNavbarToggler,
    mdbBtn,
    mdbListGroup,
    mdbListGroupItem,
    mdbIcon,
    ftr: mdbFooter
  },
  data() {
    return {
      activeItem: 1
    };
  },
  beforeMount() {
    this.activeItem = this.$route.matched[0].props.default.page;
  },
  mixins: [waves]
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap");
.navbar-light .navbar-brand {
  margin-left: 15px;
  color: #2196f3 !important;
  font-weight: bolder;
}
</style>

<style scoped>
main {
  background-color: #ededee;
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

.sidebar-fixed .logo-wrapper img {
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
