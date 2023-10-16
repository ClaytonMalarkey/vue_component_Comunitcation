<template>
  <div>
    <h2>User Profile</h2>
    <p>Name: {{ user.name }}</p>
    <p>Age: {{ user.age }}</p>
    <p>Premium: {{ user.is_premium ? 'Yes' : 'No' }}</p>
    <button @click="handleClick">CLICK ME</button>
  </div>
</template>

<script>
export default {
  props: {
    user: Object,
  },
  methods: {
    handleClick() {
      this.$emit('user_clicked', this.user.name);
    },
  },
};
</script>
