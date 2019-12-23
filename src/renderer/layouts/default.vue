<template>
  <div class="h-screen">
    <video id="bgvid" playsinline="" autoplay="" muted="" loop="" class="object-cover">

      <source src="~/assets/video.mp4#t=15" type="video/mp4">

    </video>
  	<div class="fixed flex items-center justify-between w-full py-3" v-if="$nuxt.$route.path !== '/'">
  		<nuxt-link to="/" exact><div class="ml-10 bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded">Главная</div></nuxt-link>
  		<a @click="$router.go(-1)" class="mr-10 bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded cursor-pointer">Назад</a>
  	</div>
    <nuxt />
  </div>
</template>

<style>
  video {
    position: fixed;
    top: 50%;
    left: 50%;
    min-width: 100%;
    min-height: 100%;
    width: auto;
    height: auto;
    z-index: -100;
    transform: translateX(-50%) translateY(-50%);
    background-size: cover;
    transition: 1s opacity;
}
</style>

<script>

export default {
  
}
</script>

<style>
body {
  margin: 0 !important;
}
</style>
