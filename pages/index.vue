<template>
  <div class="md:w-2/3 md:mx-auto lg:w-2/5 lg:mx-auto xl:w-1/3 xl:mx-auto">
    <div class="relative min-h-screen background">
      <div class="rounded-lg opacity-[.15] background-us min-h-screen" />
      <div class="absolute top-0 right-[42%]">
        <p class="pt-44 font-semibold text-2xl text-gray-600">بسمه تعالی</p>
      </div>
      <div class="absolute top-0 right-0 px-[24%]">
        <p class="pt-64  font-normal text-xl text-gray-500 leading-loose">
          خانه ای ساخته ایم سایبانش همه عشق زیر پا فرش غرور و حصارش همه تکرار صفا
          ما در این جمع لطیف لطف دیدار تو را می طلبم.
        </p>
      </div>
      <div class="absolute bottom-[25%] left-[40%]">
        <a href="https://goo.gl/maps/zznmRJALY3ZnFWmTA" class="text-gray-600 text-2xl font-semibold pl-9 pr-4 transition ease-out duration-700 hover:text-white hover:bg-slate-700 rounded-3xl">مسیریابی</a>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage'
})
</script>

<style scoped>
.background {
  background-image: url('../assets/images/frame.png');
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
.background-us {
  background-image: url('../assets/images/us.jpg');
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
</style>
