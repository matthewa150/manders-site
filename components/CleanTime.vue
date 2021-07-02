<template>
  <section>
    <b-container class="timeline-box">
      <b-row>
        <h3 class="timeline-head">Experiences</h3>
      </b-row>
      <b-row class="text-left">
        <ul class="list">
          <li v-for="exp in experiences" :key="exp.place">
            <span></span>
            <div class="media">
              <div class="d-flex">
                <p class="text-right">{{ exp.dates }}</p>
              </div>
              <div class="media-body">
                <h4>{{ exp.place }}</h4>
                <p>{{ exp.description }}</p>
              </div>
            </div>
          </li>
        </ul>
      </b-row>
    </b-container>
  </section>
</template>

<script>
export default {
  data () {
    return {
      experiences: [
        {
          place: 'Killer Networking',
          dates: '2015 \u2013 2018',
          description: 'Handled a myriad of tasks ranging tasks ranging from bug fixing to updating their company website. A majority of my time was spent writing internal dev. tools using Qt.'
        },
        {
          place: 'University of Texas Austin',
          dates: '2017 \u2013 present',
          description: 'Studied Computer Science and Japanese.'
        },
        {
          place: 'Tokyo Electron US',
          dates: '2019 \u2013 present',
          description: 'Developed an application to view the results of physical simulations using Qt. Benchmarked operating systems seeking improvements to the simulation cluster. Currently working on expanding and optimizing physical simulation software used for design.'
        }
      ]
    }
  }
}
</script>

<style scoped>
/* Timeline wrapper */
.timeline-box {
  margin-top: 4rem;
  flex-direction: column;
}

.timeline-head {
  margin-bottom: 2rem;
  color: #fff;
    font-size: 2rem;
  position: relative;
  text-align: center;
  margin-bottom: 3rem;
}

.timeline-head::before {
  content: "";
  position: absolute;
  height: 3px;
  background-color: rgba(255, 255, 255, 0.2);
  width: 100px;
  bottom: -12px;
  left: 50%;
  margin-left: -50px;
}

/* Timeline List */
.list {
  max-width: 460px;
  margin: auto;
  position: relative;
  padding-top: 40px;
  padding-bottom: 60px;
  padding-left: 0px;
  padding-right: 0px;
  list-style: none;
}

.list::before {
  content: "";
  height: 100%;
  width: 5px;
  background: rgba(255, 255, 255, 0.2);
  position: absolute;
  left: 46%;
  transform: translateX(-50%);
  top: -5px;
}

/* Timeline item */
.list > li {
  margin-bottom: 60px;
position: relative;
}

.list > li > span {
  height: 15px;
  width: 15px;
  border-radius: 50%;
  display: block;
  background: rgba(255, 255, 255, 0.2);
  position: absolute;
  left: 46%;
  top: 30px;
  transform: translateX(-50%);
}

.list > li > span::before {
  content: '';
  height: 7px;
  width: 7px;
  background: #fff;
  border-radius: 50%;
  position: absolute;
  left: 52%;
  top: 4px;
  transform: translateX(-50%);
}

.media {
  display: -ms-flexbox;
  display: flex;
  -ms-flex-align: start;
  align-items: flex-start;
}

/* Timeline item information */
.media-body {
  -ms-flex: 1;
  flex: 1;
}

.media-body > h4 {
  color: #fff;
  font-size: 21px;
  text-transform: uppercase;
  margin-bottom: 20px;
}

/* Timeline item date */
.d-flex > p {
  padding-top: 20px;
  width: 161px;
}

.media > .d-flex {
  padding-right: 100px;
}

/* Timeline shared info + date */
.media-body > p, .d-flex > p {
  color: rgba(255, 255, 255, 0.75);
  margin-bottom: 0px;
  margin-top: 0;
}

</style>
