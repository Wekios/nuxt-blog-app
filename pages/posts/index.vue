<template>
    <div class="posts-page">
        <Post-List :posts="loadedPosts" />
    </div>
</template>

<script>
import PostList from "~/components/Posts/PostList";

export default {
  components: {
    PostList
  },
    asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedPosts: [
        { 
          id: '1',
          title: 'First Post',
          previewText: 'This is my first post', thumbnail:'https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457' 
        },
        { 
          id: '2',
          title: 'Second Post',
          previewText: 'This is my seconde post', thumbnail:'https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457' 
        },
        { 
          id: '3',
          title: 'Third Post',
          previewText: 'This is my third post', thumbnail:'https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457' 
        },
      ]
      });
    }, 1500);
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