<template>
  <div class="contract-info">
    <img alt="Vue logo" src="../assets/logo.png">
    <SCBasicInfo msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import SCBasicInfo from '@/components/SCBasicInfo.vue'

export default {
  name: 'contract-info',
  components: {
    SCBasicInfo
  }
}
</script>
