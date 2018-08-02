<template>
  <section class="post-list">
    <post-preview
      v-for="post in posts"
      :key="post.id"
      :id="post.id" 
      :is-admin="isAdmin" 
      :thumbnail="post.thumbnail" 
      :title="post.title" 
      :previewText="post.previewText" />
  </section>
  <!-- https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457 -->
</template>

<script>
import PostPreview from "~/components/Posts/PostPreview";
export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      required: true
    }
  }
};
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>