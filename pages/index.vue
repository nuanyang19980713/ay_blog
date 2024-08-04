<template>
  <!-- 首页轮播图 -->
   <div class="w-full h-full relative">
    <el-carousel trigger="click" height="100vh">
      <el-carousel-item v-for="item in imageList" :key="item.id">
         <img :src="item.img_path" alt="图片未加载" class="w-full h-full"/>
      </el-carousel-item>
    </el-carousel>
   </div>
   <!-- 主体内容 -->
   <main class="w-4/5 m-auto flex justify-around">
      <section class="mr-5 flex-1">1</section>
      <aside class="w-1/4">2</aside>
   </main>
</template>

<script setup lang="ts">
    definePageMeta({
      layout: 'header'
    })
   useHead({
     title: "首页"
   })
   const imageList = [
    {
      id: 1,
      img_path: "/images/bg1.jfif"
    },
    {
      id: 2,
      img_path: "/images/bg2.jfif"
    },
    {
      id: 3,
      img_path: "/images/bg3.jfif"
    },
    {
      id: 4,
      img_path: "/images/bg4.jfif"
    },
    {
      id: 5,
      img_path: "/images/bg5.jfif"
    }
   ]
</script>

<style scoped lang="less">
    .el-carousel__container {
      height: 100%!important;
    }
</style>