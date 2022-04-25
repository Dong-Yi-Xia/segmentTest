<template>
  <div>
    <h1>Main</h1>
    <Header/>

    <button @click="press">click me</button>
  </div>
</template>

<script>
import config from '@/config'

export default {
  name: 'IndexPage',
  methods: {
    press(){
      analytics.track('Been press', {
        name: 'who',
        age: '9021'
      })
    }
  },
  mounted(){
    // console.log("yes", config.keys.segment)
      console.log("no", process.env.SEGMENT_KEY)
  }
}
</script>
