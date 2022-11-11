<template>
  <div
    class="w-1/3 rounded-lg border-2 p-3 shadow-lg transition duration-300 ease-in-out hover:bg-blue-300 hover:scale-105"
  >
    <!-- <div :src="getUrlImage(image)" class="w-2/3 rounded-full mx-auto" alt=""></div> -->
    
    <img :src="getUrlImage(image)" class="w-2/5 rounded-full mx-auto "  alt="">
    <div class="flex justify-between w-2/3 mx-auto">
      <div class="text-xl font-bold uppercase">My Profile</div>
      <div class="text-xl font-normal">
        <div class="text-right">{{ work }}</div>
        <div class="text-right">{{ birthday }}</div>
      </div>
    </div>

    <div class="w-2/3 mx-auto">
      <div class="text-xl font-semibold">{{ name }}</div>
      <div class="text-lg font-normal">{{ content }}</div>
    </div>

    <div class="w-2/3 mx-auto space-x-3 border-t-2 p-2">
      <font-awesome-icon icon="fa-brands fa-twitter" class="text-2xl" />
      <font-awesome-icon icon="fa-brands fa-facebook" class="text-2xl" />
      <font-awesome-icon icon="fa-brands fa-java" class="text-2xl"/>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default: "A B",
    },
    birthday: {
      type: String,
      default: "01 September 1000",
    },
    work: {
      type: String,
      default: "at home",
    },
    content: {
      type: String,
      default: "",
    },
    image: {
      type: String,
    },
  },
  methods:{
    getUrlImage(imagePath){
      return './src'+ imagePath;
    }
  }
  
};
</script>

<style>

</style>
