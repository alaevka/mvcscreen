<template>
  <div class="bg-gray-400 h-screen flex items-center justify-between w-full">
    chelovek index
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
