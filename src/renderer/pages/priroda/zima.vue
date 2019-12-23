<template>
  <div class="flex flex-wrap w-full pt-20 items-top">
    
    <div class="w-1/5 flex justify-center mb-5 image" v-for="(photo, i) in photos" :key="i" @click="index = i">
      <img class="w-40 h-40 lg:w-56 lg:h-56 xl:w-64 xl:h-64 object-cover rounded-lg border-2 border-dashed border-gray-200" :src="photo" />
    </div>
    <no-ssr placeholder="loading...">
    	<vue-gallery-slideshow :images="photos" :index="index" @close="index = null"></vue-gallery-slideshow>
    </no-ssr>
   
  </div>
</template>
<script>
import VueGallerySlideshow from 'vue-gallery-slideshow'

export default {
  data () {
    return {
      photos: [],
      index: null
    }
  },
  	components: {
  		VueGallerySlideshow
	},
  created() {
  	for (var i = 1; i <= 13; i++) {
  		this.photos.push(require('@/assets/img/priroda/zima/'+i+'.jpg'))
  	}
  },
  methods: {
    buildLogoUrl(name) {
      //return require(`@/assets/img/priroda/zima/${name}`)
    },
  }
}
</script>
