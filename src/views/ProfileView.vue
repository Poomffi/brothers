<template>
  <div class="flex items-center justify-cemter space-x-5 h-5" > </div>
    <div class ="text-red-400" v-for="member in members" :key="member" > 
      <profile-card
          v-if="member.isMember"
          :name="member.name"
          :work="member.work"
          :birthday="member.birthday"
          :content="member.content"
          :image = "member.image"
      ></profile-card>
    </div> 
  <!-- <div>
    <profile-card
      name="JobJob"
      work="at CNC2"
      birthday="25 September 2024"
      content="KU99"
      image = /assets/images/profile.jpg
    ></profile-card>
    <profile-card
      :image="image"
      :name="name"
      :work="work"
      :birthday="birthday"
      :content="content"
    ></profile-card>
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
          isMember: true,
        },
        {
          name:"JobJob",
          work:"at CNC2",
          birthday:"25 September 2024",
          content: "KU99",
          image: "/assets/images/profile.jpg",
          isMember: true,
        },
        {
          name:"poom",
          word:"nn",
          birthday:"09 11 2002",
          content: "KU81",
          image: "/assets/images/profile.jpg",
          isMember: false,
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

<style></style>
