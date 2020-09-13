<template>
  <div class="wrapper-content wrapper-content--fixed">
    <post :post="post" />
    <comments :comments="comments" />
    <newComment />
  </div>
</template>

<script>
import post from "@/components/Blog/Post.vue";
import newComment from "@/components/Comments/NewComment.vue";
import comments from "@/components/Comments/Comments.vue";
export default {
  components: { post, comments, newComment },
  data() {
    return {
      post: {
        id: 1,
        title: "1 post",
        descr:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        content:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        img:
          "https://icdn.lenta.ru/images/2020/03/25/17/20200325175249731/pwa_vertical_1024_f31bf99d62a6b93477b3322d22907449.jpg"
      },
      comments: [
        {
          name: "Alex",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        },
        {
          name: "Aaron",
          text: "Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consectetur adipiscing elit"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.post {
  max-width: 900px;
  margin: 0 auto;
}
.post-header {
  text-align: center;
  margin-bottom: 30px;
  img {
    max-width: 400px;
    margin-bottom: 16px;
  }
  p {
    color: #999;
  }
}
.post-body {
  text-align: left;
}
</style>
