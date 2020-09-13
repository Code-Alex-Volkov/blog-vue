<template>
  <div class="wrapper-content wrapper-content--fixed">
    <promo />
    <Intro title="My last posts:" />
    <PostsList :posts="postsLoaded" />
    <contacts />
  </div>
</template>

<script>
import promo from "@/components/Promo.vue";
import contacts from "@/components/Contacts.vue";

export default {
  components: { promo, contacts },
  /* asyncData(contex) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          postsLoaded: [
            {
              id: 1,
              title: "1 post",
              descr:
                "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
              img:
                "https://icdn.lenta.ru/images/2020/03/25/17/20200325175249731/pwa_vertical_1024_f31bf99d62a6b93477b3322d22907449.jpg",
            },
          ]
        })
      }, 1500);
    })
    .then(data => {
      return data
    })
    .catch(e => {
      contex.error(e)
    })
  } */
  computed: {
    postsLoaded() {
      return this.$store.getters.getPostsLoaded
    }
  }
};
</script>