<template>
  <!-- credit: https://codepen.io/Maxalos/pen/MXXqGj -->
  <section>
    <b-container class="py-2 mt-4 mb-4" style="flex-direction: column">
      <b-row v-for="(exp, idx) in experiences" :key="exp.place" no-gutters>
        <template v-if="!(idx % 2)">
          <b-col sm> <!--spacer--></b-col>
          <!--center dot-->
          <b-col class="text-center flex-column d-none d-sm-flex">
            <b-row class="h-50">
              <b-col :class="drawLine(idx, 0)">&nbsp;</b-col>
              <b-col>&nbsp;</b-col>
            </b-row>
            <h5>
              <b-badge pill>&nbsp;</b-badge>
            </h5>
            <b-row class="h-50">
              <b-col :class="drawLine(idx, 1)">&nbsp;</b-col>
              <b-col>&nbsp;</b-col>
            </b-row>
          </b-col>
        </template>
        <!-- #### item ####-->
        <b-col class="py-2">
          <b-card :title="exp.place" :sub-title="exp.dates">
            <b-card-text class="text-left">{{ exp.description }}</b-card-text>
          </b-card>
        </b-col>
        <template v-if="(idx % 2)">
          <!--center dot-->
          <b-col class="text-center flex-column d-none d-sm-flex">
            <b-row class="h-50">
              <b-col :class="drawLine(idx, 0)">&nbsp;</b-col>
              <b-col>&nbsp;</b-col>
            </b-row>
            <h5>
              <b-badge pill>&nbsp;</b-badge>
            </h5>
            <b-row class="h-50">
              <b-col :class="drawLine(idx, 1)">&nbsp;</b-col>
              <b-col>&nbsp;</b-col>
            </b-row>
          </b-col>
          <b-col sm> <!--spacer--></b-col>
        </template>
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
          description: 'Handled a myriad of tasks ranging tasks ranging from bug fixing to updating their company website. A majority of my time was spent writing internal dev. tools using Qt.'
        },
        {
          place: 'Tokyo Electron US',
          dates: '2019 \u2013 present',
          description: 'Developed an application to view the results of physical simulations using Qt. Benchmarked operating systems seeking improvements to the simulation cluster. Currently working on expanding and optimizing physical simulation software used for design.'
        }
      ]
    }
  },
  methods: {
    drawLine (idx, pos) {
      if (idx === 0 && pos === 0) {
        console.log('hit')
        return ''
      } else if (idx === this.experiences.length - 1 && pos === 1) {
        return ''
      } else {
        console.log('drawing line %i %i', idx, pos)
        return 'border-right'
      }
    }
  }
}
</script>
