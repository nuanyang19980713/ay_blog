<template>
  <header class="h-16 flex justify-between fixed w-full z-20 text-white">
     <aside class="w-3/5 flex">
         <div class="w-1/5 text-center leading-16 tracking-widest font-normal text-xl text-indigo-900">洋洋博客</div>
         <ul class="flex w-4/5 items-center">
             <li v-for="item in menuList" class="flex-1 text-center">
                 <NuxtLink :to="item.path" class="rounded-md inline-black p-3 w-3/5 h-10 hover:bg-slate-50 hover:bg-opacity-50">{{ item.name }}</NuxtLink>
             </li>
         </ul>
     </aside>
     <aside class="w-1/5"></aside>
  </header>
  <slot></slot>
</template>

<script setup lang="ts">
    import { ref } from 'vue'
    let menuList = ref([
        {
            id: 1,
            path: "/",
            name: "首页"
        },
        {
            id: 2,
            path: "/article",
            name: "文章"
        },
        {
            id: 3,
            path: "/life",
            name: "生活圈"
        },
        {
            id: 4,
            path: "/studyPath",
            name: "学习路径"
        },
        {
            id: 5,
            path: "/comment",
            name: "留言"
        }
    ])
</script>

<style>
    .router-link-active {
        background-color: rgba(255,255,255,.2);
    }
</style>