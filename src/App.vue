<template>
  <div id="app">
      <ProfileCard
        :job-title ="teams[0].jobTitle"
        :verbatim  ="teams[0].verbatim"
        :stack = "teams[0].stack"
        :profile-pic="teams[0].profilePic"
        :last-name = "teams[0].lastName"
        :first-name = "teams[0].firstName"
      />
  </div>
</template>

<script>
import {teams}        from './assets/static/js/appTeams.js'
import ProfileCard    from './components/ProfileCard.vue'

export default {
  name: 'App',
  components: {
      ProfileCard
  },
  data:()=>({
        teams,
        insideMethodsData:'Choupichou'
  }),
  methods:{

  }
}
</script>

<style>


</style>
