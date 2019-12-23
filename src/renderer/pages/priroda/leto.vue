<template>
  <div class="h-full flex items-center justify-between w-full">
    leto
  </div>
</template>
<script>
import { remote } from 'electron'

export default {
  components: {
    
  },
  data () {
    return {
      externalContent: ''
    }
  },
  methods: {
    openURL (url) {
      remote.shell.openExternal(url)
    }
  }
}
</script>
