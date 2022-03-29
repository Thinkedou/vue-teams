<template>
    <div class="stat">
        <div class="techno">{{stackLabel}}</div>
        <div class="level">{{displayStars()}}</div>
    </div>
</template>

<script>
export default {
  name: 'StackDisplay',
  props: {
      stackLabel:{
          type:String
      },
      stackLevel:{
          type:Number
      }
  },
  data:()=>({

  }),
  methods:{
      displayStars(){
          const STARS = '✨'
          return STARS.repeat(this.stackLevel)
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
