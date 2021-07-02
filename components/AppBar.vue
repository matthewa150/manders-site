<template>
  <b-navbar :fixed="fixedTo" :class="customStyle" type="dark">
    <b-container>
      <b-navbar-brand>
        <span class="font-weight-bold">Matthew</span>
        <span class="font-weight-light">Anderson</span>
      </b-navbar-brand>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="https://github.com/matthewa150">GitHub</b-nav-item>
        <b-nav-item href="https://www.linkedin.com/in/matthew-anderson-a65063148">LinkedIn</b-nav-item>
        <b-nav-item href="manders_cv.pdf" target="_blank">My CV</b-nav-item>
      </b-navbar-nav>
    </b-container>
  </b-navbar>
</template>

<script>
export default {
  props: {
    fixedTo: {
      type: String,
      require: false,
      default: 'null'
    },
    customStyle: {
      type: String,
      require: false,
      default: ''
    }
  }
}
</script>

<style scoped>
.navbar-dark .navbar-nav .nav-link {
  color: white
}
</style>
