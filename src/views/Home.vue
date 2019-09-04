<template>
  <div class="home">
  	<FirstPage/>
   
  </div>
</template>

<script>
// @ is an alias to /src
import FirstPage from '@/components/FirstPage.vue'

export default {
  name: 'home',
  components: {
    FirstPage
  }
}
</script>
