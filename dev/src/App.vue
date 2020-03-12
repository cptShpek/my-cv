<template>
  <div>

    <MainSection />
    <hr>

    <h2>Summary</h2>
    <hr>
    <Summary v-bind:skills="mySummary"></Summary>
    <hr>

    <h2>Work Experience</h2>
    <hr>
    <button v-for="job in mySummary.jobs" :key="job" @click="showJob( job.position )"><h3>{{job.position}}</h3></button>
    <div>
    <transition-group name="jobs" tag="div">
      <myJobs v-for="job in mySummary.jobs" :key="job.position" v-bind:job="job" :id="job.position" :class="job.position"></myJobs>
    </transition-group>
    </div>
    <hr width="75%">

  </div>
</template>

<script>

import MainSection from "./components/MainSection"
import Summary from "./components/Summary"
import {mySummary} from "./components/personalInfo/info"
import MyJobs from "./components/MyJobs"


export default {

  name: 'App',

  components: {
    MainSection,
    Summary,
    MyJobs
  },

  data() {
    return{
      mySummary,
      myJobs: [ "LinkBuilder", "SEO", "TeamLead" ]
    }
  },

  methods: {

    showJob ( id ) {

      for ( let position of this.myJobs ) {

        if ( position == id ) {

          document.getElementById( id ).style.display = "block"

        } else {

          document.getElementById( position ).style.display = "none"


        }

      }

    },

  }

}
</script>

<style>

  .SEO, .TeamLead {

    display: none;

  }

  .SEO, .TeamLead, .LinkBuilder {

    height: 300px;

  }

  .jobs-enter, .jobs-leave-to {
    transition: transform 1s;
  }

</style>
