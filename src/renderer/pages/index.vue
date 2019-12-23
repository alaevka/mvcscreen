<template>
  <div class="h-full flex items-center justify-around">
    <div class="w-1/3 flex justify-center">
      <nuxt-link to="/priroda" exact>
        <div class="text-center">
          <div><img class="w-40 h-40 lg:w-56 lg:h-56 xl:w-64 xl:h-64 object-cover rounded-full border-2 border-dashed border-gray-200" src="~/assets/img/priroda/leto/1.jpg" /></div>
          <div class="bg-gray-200 py-2 px-3 opacity-50 rounded-lg mt-2"><h2 class="opacity-100 font-bold">ПРИРОДА</h2></div>
        </div>
      </nuxt-link>
    </div>
    <div class="w-1/3 flex justify-center">
      <nuxt-link to="/gorod" exact>
        <div class="text-center">
          <div><img class="w-40 h-40 lg:w-56 lg:h-56 xl:w-64 xl:h-64 object-cover rounded-full border-2 border-dashed border-gray-200" src="~/assets/img/gorod/ulici/lenina/lenina_1-5.jpg" /></div>
          <div class="bg-gray-200 py-2 px-3 opacity-50 rounded-lg mt-2"><h2 class="opacity-100 font-bold">ГОРОД</h2></div>
        </div>
      </nuxt-link>
    </div>
    <div class="w-1/3 flex justify-center">
      <nuxt-link to="/chelovek" exact>
        <div class="text-center">
          <div>
            <img class="w-40 h-40 lg:w-56 lg:h-56 xl:w-64 xl:h-64 object-cover rounded-full border-2 border-dashed border-gray-200" src="~/assets/img/chelovek/cultura/muzei/1.jpg" />
          </div>
          <div class="bg-gray-200 py-2 px-3 opacity-75 rounded-lg mt-2"><h2 class="opacity-100 font-bold">ЧЕЛОВЕК</h2></div>
        </div>
      </nuxt-link>
    </div>
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
