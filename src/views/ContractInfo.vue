<template>
  <div class="contract-info">
    <SmartContractInfo/>
  </div>
</template>

<script>
// @ is an alias to /src
import SmartContractInfo from '@/components/SmartContractInfo.vue'

export default {
  name: 'contract-info',
  components: {
    SmartContractInfo
  }
}
</script>
