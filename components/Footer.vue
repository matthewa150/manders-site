<template>
  <footer>
    <div class="footer mt-3 pt-4 pb-2">
      <b-container>
        <b-row align-v="center">
          <b-col class="text-left" xs="12" sm="6">
            <h5 class="quiet-head">About this site</h5>
            <p class="quiet-text">
              This website is built using <a class="quiet-link" href="https://nuxtjs.org/">NuxtJS</a>
              and <a class="quiet-link" href="https://bootstrap-vue.org/">BootstrapVue</a>. The background
              was generated using a <a class="quiet-link" href="https://cojdev.github.io/lowpoly/">
              low poly generator</a>, and the color scheme from a
              <a class="quiet-link" href="https://colordesigner.io/gradient-generator">gradient generator</a>.
              Inspiration was drawn from the <a class="quiet-link" href="https://colorlib.com/wp/template/calvin/">
              Calvin</a> and <a class="quiet-link" href="https://colorlib.com/wp/template/meetme/">Meetme</a> themes.
            </p>
          </b-col>
          <b-col />
          <b-col class="text-right">
          </b-col>
        </b-row>
      </b-container>
    </div>
  </footer>
</template>

<style scope>
.footer {
  color: rgba(255, 255, 255, 1.0);
  background-color: black;
}

.quiet-head {
  color: #ccc;
  font-size: 1.0rem;
}

.quiet-text {
  color: #777;
  font-size: 0.7rem;
}

.quiet-link {
  color: #aaa;
}

.quiet-button {
  color: #aaa;
  border-color: #aaa;
}
</style>
