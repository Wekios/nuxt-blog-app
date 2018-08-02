<template>
  <div class="home-page">
    <section class="intro">
      <h1>Howdy</h1>
    </section>
    <PostList :posts="loadedPosts"/>
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
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url("~assets/images/main-page-background-img.jpg");
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>