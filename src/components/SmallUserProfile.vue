<template>
  <div>
    <h2>User Profile</h2>
    <p>Name: {{ user.name }}</p>
    <p>Age: {{ user.age }}</p>
    <p>Premium: {{ user.is_premium ? 'Yes' : 'No' }}</p>
  </div>
</template>

<script>
export default {
  props: {
    user: Object,
  },
};
</script>