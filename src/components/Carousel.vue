<template>
  <div class="container">
    <div
      class="carousel slide carousel-swipe"
      ref="swipe"
      id="carousel"
      data-ride="carousel"
      data-interval="10000"
    >
      <ol class="carousel-indicators">
        <li class="active" data-target="#carousel" data-slide-to="0"></li>
        <li
          data-target="#carousel"
          :key="index"
          v-for="index of images.length"
          :data-slide-to="index + 1"
        ></li>
      </ol>
      <div class="carousel-inner" role="listbox">
        <div
          :class="{ active: index == 0, item: true }"
          :key="index"
          v-for="(image, index) in images"
        >
          <img :src="image.img" />
          <div class="carousel-caption">{{ image.caption }}</div>
        </div>
      </div>
      <a
        class="left carousel-control"
        href="#carousel"
        role="button"
        data-slide="prev"
        ><span
          class="glyphicon glyphicon-chevron-left"
          aria-hidden="true"
        ></span
        ><span class="sr-only">Prev</span></a
      ><a
        class="right carousel-control"
        href="#carousel"
        role="button"
        data-slide="next"
        ><span
          class="glyphicon glyphicon-chevron-right"
          aria-hidden="true"
        ></span
        ><span class="sr-only">next</span></a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "Carousel",
  props: {
    images: Array,
  },
};
</script>

<style>
.carousel-caption {
  background: rgba(0, 0, 0, 0.3);
  padding: 15px;
  margin: 0;
  font-size: 19px;
  margin-bottom: 40px;
}
.carousel-progress {
  position: absolute;
  bottom: 0;
  left: 0;
  background: rgba(black, 0.3);
  display: block;
  width: 100%;
  height: 5px;
}
img {
  width: 100%;
}
</style>