<template>
  <div id="app">
    <router-view/>
    <cfooter></cfooter>
  </div>
</template>
<script>
import Cfooter from "@/components/Cfooter.vue"
export default {
  components:{
    Cfooter
  }
}
</script>

