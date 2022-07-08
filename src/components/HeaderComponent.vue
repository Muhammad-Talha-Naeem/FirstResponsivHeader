<template>
  <div>
    <header class="text-gray-600 bg-red-300 body-font">
      <div
        class="container mx-auto flex flex-wrap md:flex-row justify-between items-center"
      >
        <a href="#" class="flex title-font font-medium items-center text-gray-900 md:mb-0">
          <img src="" class="w-[20px] h-[20px]" alt="" />
          <span class="ml-3 text-xl">SiteName</span>
        </a>
        <nav
          id="lg-nav"
          class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center"
        >
          <a href="#" class="mx-2 p-1 hover:text-gray-900">First Link</a>
          <a href="#" class="mx-2 p-1 hover:text-gray-900">Second Link</a>
          <a href="#" class="mx-2 p-1 hover:text-gray-900">Third Link</a>
          <a href="#" class="mx-2 p-1 hover:text-gray-900">Fourth Link</a>
        </nav>
        <div>
          <div @mouseenter="showbtn" @mouseleave="hidebtn" class="hover:bg-gray-200 rounded px-1">
            <font-awesome-icon icon="fas fa-circle-user" size="lg" />
            <a href="#"
            id="btn"
              class="hidden  items-center border-0 px-1 focus:outline-none hover:bg-gray-200 rounded text-base"
            >
              Button

              <font-awesome-icon icon="fas fa-arrow-right" class="pl-1" />
            </a>
          </div>
        </div>
      </div>
      <div>
        <nav id="xs-nav" class="hidden mx-auto flex-wrap text-base justify-center">
          <a href="#" class="mx-2 p-1 hover:text-gray-900">First Link</a>
          <a href="#" class="mx-2 p-1 hover:text-gray-900">Second Link</a>
          <a href="#" class="mx-2 p-1 hover:text-gray-900">Third Link</a>
          <a href="#" class="mx-2 p-1 hover:text-gray-900">Fourth Link</a>
        </nav>
      </div>
    </header>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "App",
  methods:{
    showbtn:()=>document.querySelector(`#btn`)?.classList.remove(`hidden`),
    hidebtn:()=>document.querySelector(`#btn`)?.classList.add(`hidden`)
  }
});
</script>

<style scoped>
@media only screen and (max-width: 645px) {
  #lg-nav {
    display: none;
  }
  #xs-nav {
    display: flex;
  }
}
@media only screen and (max-width: 405px) {
  #xs-nav {
    display: flex;
    flex-direction: column;
  }
}
</style>
