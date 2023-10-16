<template>
  <div>
    <h1>User Profiles</h1>
    <div v-for="user in users" :key="user.id">
      <SmallUserProfile :user="user" />
    </div>
  </div>
</template>

<script>
import SmallUserProfile from './components/SmallUserProfile.vue'; // Import the SmallUserProfile component

export default {
  components: {
    SmallUserProfile, // Register the SmallUserProfile component
  },
  data() {
    return {
      users: [
        { name: 'User1', age: 25, is_premium: true, id: 1 },
        { name: 'User2', age: 30, is_premium: false, id: 2 },
        // Add more users as needed
      ],
    };
  },
};
</script>
