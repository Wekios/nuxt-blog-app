<template>
  <section class="post-list">
    <post-preview id="1" :is-admin="isAdmin" thumbnail="https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457" title="Hello there!" previewText="howdy" />
    <post-preview id="2" :is-admin="isAdmin" thumbnail="https://inm-baobab-prod-eu-west-1.s3.amazonaws.com/public/inm/media/image/2017/10/18/38770746IOLmotOct18KwidX.jpg" title="Hello this is my second post" previewText="howdy this is my second post and bla bla!!! " />
    <post-preview id="3" :is-admin="isAdmin" thumbnail="https://e3.365dm.com/18/03/1096x616/skynews-renault-car-generic_4267669.jpg?bypass-service-worker&20180329120457" title="Thirdo Posto!" previewText="howdy this is my LAST FUCKING POST -OAOSPKMDPASMDOIASNDIMNA " />
  </section>
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