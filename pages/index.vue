<template>
  <div>
    <transition name="slide-fade">
      <AppBar v-if="showBar" fixedTo="top" customStyle='thin-solid' />
    </transition>
    <AboutHeader />
    <CleanTime />
    <!-- Ideas: blog posts, project highlights -->
    <Footer />
  </div>
</template>

<script>
export default {
  data () {
    return {
      showBar: false
    }
  },
  mounted () {
    window.onscroll = () => {
      this.changeAppBar()
    }
  },
  methods: {
    changeAppBar () {
      if (document.body.scrollTop > 300 || document.documentElement.scrollTop > 300) {
        this.showBar = true
      } else {
        this.showBar = false
      }
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.links {
  padding-top: 15px;
}

body {
  /*background-color: rgb(245,245,245);*/
  /*background-image: -webkit-linear-gradient(0deg, #766dff 0%, #88f3ff 100%);*/
  background-image: url('/lowpoly.png');
  background-size: cover;
  background-attachment: fixed;
}
</style>
