<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/Admin/AdminPostForm";
export default {
  data() {
    return {
      loadedPost: {
        author: "Veljko",
        title: "Awesome Post",
        content: "Super Amazing ",
        thumbnailLink:
          "https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457"
      }
    };
  },
  components: {
    AdminPostForm
  }
};
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}
@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>