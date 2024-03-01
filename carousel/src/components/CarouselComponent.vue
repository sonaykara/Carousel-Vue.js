<template>
  <div>
    <carousel-slide :carouselItems="carouselItems"></carousel-slide>
  </div>
</template>

<script>
import CarouselSlide from "./CarouselSlide.vue";
import img_1 from "../assets/114-1000x600.jpg";
import img_2 from "../assets/539-1000x600.jpg";
import img_3 from "../assets/543-1000x600.jpg";
import img_4 from "../assets/554-1000x600.jpg";
import img_5 from "../assets/656-1000x600.jpg";

export default {
  data() {
    return {
      carouselItems: [
        {
          img: img_1,
          subtitle: "Lorem",
          title: "Sed do eiusmod tempor incididunt",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
        },
        {
          img: img_2,
          subtitle: "İpsum",
          title: "Incididunt ut labore et doloret",
          description: "Excepteur sint occaecat cupidatat non proident",
        },
        {
          img: img_3,
          subtitle: "Dolor",
          title: "Laboris nisi ut aliquip ex",
          description:
            "Ut enim ad minim veniam, quis nostrud exercitation ullamco",
        },
        {
          img: img_4,
          subtitle: "Amet",
          title: "Velit esse cillum dolore eu fugiat",
          description: "Excepteur sint occaecat cupidatat non proident",
        },
        {
          img: img_5,
          subtitle: "Eiusmod",
          title: "Officia deserunt mollit anim id",
          description:
            "sunt in culpa qui officia deserunt mollit anim id est laborum",
        },
      ],
    };
  },

  components: {
    CarouselSlide,
  },
};
</script>

<style lang="scss" scoped></style>
