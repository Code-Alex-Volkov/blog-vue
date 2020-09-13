<template>
  <div class="wrapper-content wrapper-content--fixed">
    <promo />
    <Intro title="My last posts:" />
    <PostsList :posts="posts" />
    <contacts />
  </div>
</template>

<script>
import promo from "@/components/Promo.vue";
import contacts from "@/components/Contacts.vue";

export default {
  components: { promo, contacts },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "1 post",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
          img:
            "https://icdn.lenta.ru/images/2020/03/25/17/20200325175249731/pwa_vertical_1024_f31bf99d62a6b93477b3322d22907449.jpg"
        },
        {
          id: 2,
          title: "2 post",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          img:
            "https://www.thoughtco.com/thmb/GioEradeSi02cirgRzFjZLP23DI=/2121x1414/filters:fill(auto,1)/dog-2f28db29d6ef4f7a946629bac11ac41e.jpg"
        },
        {
          id: 3,
          title: "3 post",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.",
          img:
            "https://cs2.livemaster.ru/storage/c5/9d/76a830b359d837b6f3f616e6318k--author-s-patterns-mk-at-the-elm-th-brooch-out-of-the-pocket-d.jpg"
        }
      ]
    };
  }
};
</script>