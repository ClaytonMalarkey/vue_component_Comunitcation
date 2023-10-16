<template>
  <div>
    <h1>User Profiles</h1>
    <h1 v-if="clickedUserName">{{ clickedUserName }}</h1>

    <div v-for="user in users" :key="user.id">
      <SmallUserProfile :user="user" @user_clicked="handleUserClicked" />
    </div>
  </div>
</template>

<script>
import SmallUserProfile from './components/SmallUserProfile.vue';

export default {
  components: {
    SmallUserProfile,
  },
  data() {
    return {
      users: [
        { name: 'User1', age: 25, is_premium: true, id: 1 },
        { name: 'User2', age: 30, is_premium: false, id: 2 },
        // Add more users as needed
      ],
      clickedUserName: null,
    };
  },
  methods: {
    handleUserClicked(username) {
      this.clickedUserName = username;
    },
  },
};
</script>
