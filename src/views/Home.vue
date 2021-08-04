<template>
  <div class="home">
    <contents/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import contents from '@/components/content.vue'

export default {
  name: 'Home',
  components: {
    // HelloWorld,
    contents
  }
}
</script>
