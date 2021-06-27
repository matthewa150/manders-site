<template>
  <section>
    <b-container class="sect-pt4">
      <b-row class="full-row">
        <b-col sm="12">
          <b-card class="info-card">
            <b-row>
              <b-col md="6">
                <b-row>
                  <b-col md="5" sm="6">
                    <b-img fluid rounded src="profile.jpg" alt="Profile Picture"/>
                  </b-col>
                  <b-col md="7" sm="6" class="text-left">
                    <div class="about-info">
                      <p v-for="info in aboutInfo" :key="info.aspect">
                        <span class="title-s">
                          {{ info.aspect }}:
                        </span>
                        <span>
                          {{ info.data }}
                        </span>
                      </p>
                    </div>
                  </b-col>
                </b-row>
              </b-col>
              <b-col md="6">
                <h5 class="about-title">
                  About me
                </h5>
              </b-col>
            </b-row>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script>
export default {
  data () {
    return {
      aboutInfo: [
        {
          aspect: 'Name',
          data: 'Matthew Anderson'
        },
        {
          aspect: 'Profile',
          data: 'Software Engineer'
        },
        {
          aspect: 'Email',
          data: 'matthewa150@gmail.com'
        },
        {
          aspect: 'Phone',
          data: '(512) 568-5098'
        }
      ]
    }
  }
}
</script>

<style>
.sect-pt4 {
  padding-top: 4rem;
  min-height: 0;
}

.info-card {
  padding-top: 4rem;
  padding-bottom: 4rem;
}

.title-s {
  font-size: 1.1rem;
  font-weight: 600;
}

.about-title::before {
  content: "";
  position: absolute;
  height: 3px;
  background-color: var(--secondary);
  width: 100px;
  bottom: -12px;
  left: 50%;
  margin-left: -50px;
}

.about-title {
  font-size: 2rem;
  position: relative;
  text-align: center;
  margin-bottom: 3rem;
}

.full-row {
  width: calc(100% + 30px);
}
</style>
