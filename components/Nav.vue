<template>
  <div class="nav-custom">
    <b-navbar
      toggleable="lg"
      type="light"
      fixed="top"
      class="animate__animated animate__fadeInDown"
    >
      <b-navbar-brand to="/">
        <img
          src="@/static/ragazza2026.webp"
          class="d-inline-block align-middle logo__gc"
          alt="Kitten"
        />
      </b-navbar-brand>

      <!-- <b-navbar-toggle target="nav-collapse"></b-navbar-toggle> -->
      <b-navbar-nav to="/"> </b-navbar-nav>

      <b-navbar-nav>
        <b-nav-item href="#" v-b-toggle.sidebar-right class="h6">
          <b-icon-search></b-icon-search>
        </b-nav-item>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
import SearchForm from "~/components/SearchForm";
import Sidebar from "~/components/Sidebar";

export default {
  name: "Navbar",
  components: {
    SearchForm,
    Sidebar
  }
};
</script>
