<template>
  <div class="flex items-center justify-cemter space-x-5 h-5 " ></div>

  
  <div class ="text-red-400 flex flex-row grid-container"> 
    <profile-card
    v-for="member in members" 
    class="basis-1/3 m-5 bg-blue-200 "
    :key="member"
    :name="member.name"
    :work="member.work"
    :birthday="member.birthday"
    :content="member.content"
    :image = "member.image" 
    ></profile-card>
  </div>
  
  <video autoplay loop muted class="video" src="https://i.gifer.com/WAE8.mp4"></video>

  
  

  <!-- <div class="grid-container">
    <div>
      <profile-card
      name="JobJobasdf"
      work="at CNC2"
      birthday="25 September 2024"
      content="KU99"
      image = /assets/images/profile.jpg
      ></profile-card>
    </div>
    <div>
      <profile-card
      name="JobJobasdf"
      work="at CNC2"
      birthday="25 September 2024"
      content="KU81"
      image = /assets/images/profile.jpg
      ></profile-card>
    </div>
    <div>
      <profile-card
      name="JobJobasdf"
      work="at CNC2"
      birthday="25 September 2024"
      content="KU81"
      image = /assets/images/profile.jpg
      ></profile-card>
    </div>
  </div> -->
    
    

</template>

<script>
import profileCard from "../components/Profile.vue";
export default {
  data() {
    return {
      members: [
        {
          name: "Narongrit",
          birthday: "25 September 2022",
          work: "work at CNC",
          content: "KU79",
          image: "/assets/images/profile.jpg",
          
        },
        {
          name:"JobJob",
          work:"at CNC2",
          birthday:"25 September 2024",
          content: "KU99",
          image: "/assets/images/profile.jpg",
          
        },
        {
          name:"poom",
          word:"nn",
          birthday:"09 11 2002",
          content: "KU81",
          image: "/assets/images/profile.jpg",
        
        }
    ]
    // ,
    //   name: "Narongrit",
    //   birthday: "25 September 2022",
    //   work: "work at CNC",
    //   content: "KU79",
    //   image: "/assets/images/profile.jpg",
    };
  },
  components: {
    profileCard,
  },
};
</script>

<style>
  .grid-container {
  display: grid;
  /* background-color: #6bb5f5; */
  /* padding: 15px; */
  margin-left: 35px;
  margin-right: 35px;
  border-radius: 15px;
  height: 640px;
  }
  .video{
    z-index: -1000;
    left: 50%;
    width: 100vw;
    height: 100vh;
    position: absolute;
    top: 50%;
    -webkit-transform: translate(-50%, -50%);
    -moz-transform: translate(-50%,-50%);
    -ms-transform: translate(-50%,-50%);
    transform: translate(-50%,-50%);
    object-fit: cover;
  }
</style>
