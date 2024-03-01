<template>
  <div>
    <div class="carousel-area">
      <div
        class="carousel"
        v-for="(carousel, index) in carouselItems"
        :key="index"
      >
        <div class="carousel-positon" v-if="currentItem === index">
          <div class="carousel-area">
            <img :src="carouselItems[index].img" alt="" />
            <div class="information-area">
              <h1>{{ carousel.subtitle }}</h1>
              <p>{{ carousel.title }}</p>
              <p>{{ carousel.description }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="btn-area">
        <div class="btn">
          <div>
            <i class="bi bi-arrow-left-circle-fill" @click="prevItem"></i>
          </div>
          <div>
            <i class="bi bi-arrow-right-circle-fill" @click="nextItem"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    carouselItems: {
      type: Array,
    },
  },
  data() {
    return {
      currentItem: 0,
    };
  },

  methods: {
    nextItem() {
      this.currentItem = (this.currentItem + 1) % this.carouselItems.length;
    },

    prevItem() {
      this.currentItem =
        (this.currentItem - 1 + this.carouselItems.length) %
        this.carouselItems.length;
    },
  },
};
</script>

<style scoped>
.carousel {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  
  .carousel-area {
    position: relative;
  }
  
  .information-area {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 2rem;
    font-size: 2rem;
    color: #374956;
  }
  
  .information-area p {
    font-size: 2rem;
    color: #4e88b1;
  }
  
  .btn-area {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .btn {
    display: flex;
    gap: 56rem;
  }
  
  i {
    font-size: 2rem;
    color: #4e88b1;
  }
</style>
