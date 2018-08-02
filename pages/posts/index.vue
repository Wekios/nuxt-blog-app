<template>
    <div class="posts-page">
        <Post-List/>
    </div>
</template>

<script>
import PostList from "~/components/Posts/PostList";
export default {
  components: {
    PostList
  }
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>