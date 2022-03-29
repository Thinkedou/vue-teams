<template>
  <div id="app">

      <div class="card">
          <div class="card-image"></div>
          <div class="card-text">
            <span class="job">{{teams[0].jobTitle}}</span>
            <h2>FirstName &amp; LastName</h2>
            <p>Petit Laïus</p>
          </div>
          <div class="card-stats">
            <div class="stat">
              <div class="techno">{{teams[0].stack[0].label}}</div>
              <div class="level">{{displayLevel(teams[0].stack[0].level)}}</div>
            </div>
            <div class="stat border">
              <div class="techno">Techno</div>
              <div class="level">⭐⭐⭐</div>
            </div>
          </div>
        </div>

  </div>
</template>

<script>
import {teams} from './assets/static/js/appTeams.js'

export default {
  name: 'App',
  components: {
  },
  data:()=>({
      teams,
      insideMethodsData:'Choupichou'
  }),
  methods:{
      displayLevel(level){
          const starString = '⭐'
          return starString.repeat(level)
      },
      preFormat(){
          return true
      }
  }
}
</script>

<style>
@import './assets/static/css/card-styles.css';

</style>
