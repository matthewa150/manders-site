<template>
  <section>
    <!-- ############## -->
    <!-- # Static Bar # -->
    <!-- ############## -->
    <div class="py-3">
      <AppBar />
    </div>
    <!-- ######### -->
    <!-- # Intro # -->
    <!-- ######### -->
    <div>
      <b-container>
        <b-row align-v="center">
          <b-col sm="4">
            <b-img fluid rounded="circle" src="profile.jpg" alt="Profile Picture" class="profile-pic"/>
          </b-col>
          <b-col sm="8">
            <div class="h-100 big-header">
              <h1>
                I am Matthew Anderson
              </h1>
              <h3>
                <vue-typer
                  :text='["Software Engineer","College Student","Japanese Speaker","Baseball Fan"]'
                  :repeat='Infinity'
                  :shuffle='true'
                  initial-action='typing'
                  :pre-type-delay='70'
                  :type-delay='70'
                  :pre-erase-delay='2000'
                  :erase-delay='35'
                  erase-style='backspace'
                  :erase-on-complete='false'
                  caret-animation='blink'
                ></vue-typer>
              </h3>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <!-- ############ -->
    <!-- # About Me # -->
    <!-- ############ -->
    <div class="about-me py-3">
      <b-container>
        <b-card class="w-100 text-left">
          <b-row align-h="center" align-v="center">
            <b-col sm="6">
              <div>
                <h2 class="about-title">
                  About Me
                </h2>
              </div>
              <div class="" v-for="line in about" :key="line">
                <p class="font-weight-light">
                  {{ line }}
                </p>
              </div>
            </b-col>
            <b-col sm="6">
              <div class="py-2" v-for="skill in skills" :key="skill.lang">
                <span>{{ skill.lang }}</span>
                <span class="float-right">{{ skill.prof }}%</span>
                <b-progress class="mt-1">
                  <b-progress-bar class="progress-towards" :value="skill.prof" />
                  <b-progress-bar class="progress-against" :value="100 - skill.prof" />
                </b-progress>
              </div>
            </b-col>
            <b-col sm="6" class="d-flex justify-content-between">
              <div>
                <a href="mailto: matthewa150@gmail.com">
                  <b-icon icon="mailbox"></b-icon>
                  <span class="font-weight-light">
                    matthewa150@gmail.com
                  </span>
                </a>
              </div>
              <div>
                <a href="tel:+1512-568-5098">
                  <b-icon icon="phone-vibrate"></b-icon>
                  <span class="font-weight-light">
                    (512) 568-5098
                  </span>
                </a>
              </div>
            </b-col>
          </b-row>
        </b-card>
      </b-container>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      about: [
        'I am a native Texan, born and raised, attending the University of Texas at Austin. I am pursuing a B.S. in Computer Science (as a Turing Scholar), as well as B.A. in Asian Studies (Japanese).',
        'I started programming as a freshman in high school, and I have loved it ever since. I became interested in learning Japanese after spending a month in Tokyo.',
        'In my free time I enjoy playing video games, reading science fiction, and watching baseball games.'
      ],
      skills: [
        {
          lang: 'C/C++',
          prof: 80
        },
        {
          lang: 'Python',
          prof: 85
        },
        {
          lang: 'HTML/CSS/JS/SQL',
          prof: 70
        }
      ]
    }
  }
}
</script>

<style>
.profile-pic {
  outline: 3px solid white;
  outline-offset: 5px;
  margin: 10px;
}

.big-header, .vue-typer .custom.char {
  color: white;
}

.vue-typer .custom.caret {
  background-color: white;
}

.about-me {
  margin-top: 30px;
}
</style>
