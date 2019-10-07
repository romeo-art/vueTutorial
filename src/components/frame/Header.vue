<template>
  <div fixed="top">
    <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand href="#" id="title">MYAPP</b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
  <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item v-on:click="redirect('/Login')" v-if="auth.user ===null"  id="login">Login</b-nav-item>
        <b-nav-item v-on:click="redirect('/Register')" v-if="auth.user ===null"  id="signup">Register</b-nav-item>
      </b-navbar-nav>
  </b-collapse>
    </b-navbar>
</div>
</template>

<style scoped lang="scss">
@import "assets/style.scss";

#background {
  background-color: #ffc299;
}
</style>
<script>
import AUTH from 'services/auth'
import ROUTER from "router";
export default {
  data(){
    return {
      auth: AUTH
    }
  },
  methods: {
    redirect(router) {
      ROUTER.push(router);
    }
  }
};
</script>
