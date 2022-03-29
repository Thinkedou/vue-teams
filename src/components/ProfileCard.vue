<template>
    <div class="card"  >
        <div class="card-image" :style="{ backgroundImage: `url(${require('../assets/static/img/'+profilePic)})` }"></div>
        <div class="card-text">
          <span class="job">{{jobTitle}}</span>
          <h2>{{firstName}} {{lastName}}</h2>
          <p>{{verbatim}}</p>
        </div>
        <div class="card-stats">

           <StackDisplay
                :stack-label="stack[0].label"
                :stack-level="stack[0].level"
           />
           <StackDisplay
               :stack-label="stack[1].label"
               :stack-level="stack[1].level"
               class='border'
           />

        </div>
      </div>

</template>

<script>
import StackDisplay from './StackDisplay.vue'

export default {
  name: 'ProfileCard',
  components:{
      StackDisplay
  },
  props: {
        jobTitle:{
            type:String
        },
        firstName:{
            type:String
        },
        lastName:{
            type:String
        },
        verbatim:{
            type:String
        },
        profilePic:{
            type:String
        },
        stack:{
            type:Array
        }

  },
  data:()=>({

  }),
  methods:{

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '@/assets/static/css/card-styles.css';
@import url('https://fonts.googleapis.com/css?family=Muli&display=swap');


</style>
