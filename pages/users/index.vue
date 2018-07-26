<template>
    <div>
      <input v-model="userId" type="text" />
      <button @click="onLoadUser"> 
      Go to user
      </button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      userId: ""
    };
  },
  methods: {
    onLoadUser() {
      this.$router.push("/users/" + this.userId);
    }
  }
};
</script>

<style scoped>
</style>