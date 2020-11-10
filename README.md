# vue-carousel-bootstrap
A simple Vue Carousel based on bootstrap carousel 
## Demo 
https://csb-w80hp.vercel.app/

## how to use 

you can fork this project
and use the Carousel component

you can find the location of the component in [./src/components/Carousel.vue](./src/components/Carousel.vue)


## example 
```
<template>
  <div id="app">
    <h1>Simple Carousel Implementation</h1>
    <Carousel :images="images" />
  </div>
</template>

<script>
import Carousel from "./components/Carousel";

export default {
  name: "App",
  components: {
    Carousel,
  },
  data() {
    return {
      images: [
        {
          caption: "First",
          text: "Image 1 ",
          img: "https://picsum.photos/1024/480/?image=52",
        },
        {
          caption: "Second",
          text: "Image 2 ",
          img: "https://picsum.photos/1024/480/?image=42",
        },
        {
          caption: "Third",
          text: "Image 3 ",
          img: "https://picsum.photos/1024/480/?image=52",
        },
        {
          caption: "Fourth",
          text: "Image 4 ",
          img: "https://picsum.photos/1024/480/?image=51",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

```
## configuration 
the components expects a list of images object as a prop
each image is an object with this required two properties 
+ `img` the src url of the image to used 
+ `caption`  the caption to be used for the image

## TODO 
+ [ ] add more example 
+ [ ] add more config props 
+ [ ] add new features and extend the component
+ [ ] deploy to npm as a package
