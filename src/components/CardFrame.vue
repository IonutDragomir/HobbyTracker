<template>
  <div class="wrapper" @mouseover="title = true" @mouseout="title = false">
    <div class="image_container pt-2">
      <img :src="imgUrl" :alt="name + ' picture'">
    </div>
    <section class="info_container">
      <header class="pt-3 ps-2 mb-3">
        <h2>{{ name }}</h2>
      </header>
      <p class="ps-2" :style="date == 'TBA' ? 'font-style: italic' : ''">{{ date }}</p>
      <p class="ps-2 pb-3">price</p>
    </section>

  </div>
</template>

<script>
import "bootstrap";

export default {
  name: "HelloWorld",
  props: ["details"],
  mounted() {
    // console.log(this.name);
  },
  data() {
    return {
      name: this.details.name,
      imgUrl: this.details.imageUrl,
      title: false,
      date: this.details.release_date,
      fontSize: 35
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~bootstrap/dist/css/bootstrap.css";

.wrapper {

  .image_container {
    img {
      width: 12vw;
      height: 7vw;
      object-fit: fill;
      border-radius: 1vw;
    }
  }

  .info_container {
    text-align: left;

    header {

      h2 {
        font-size: 21px;
        line-height: initial;
      }
    }

    p {
      font-size: 18px;
      line-height: initial;
      margin: 0;
    }
  }

}

.wrapper:hover {
  box-shadow: rgba(0, 0, 0, 0.24) -9px -3px 8px, rgba(0, 0, 0, 0.24) 6px 3px 8px;
  border-radius: 1vw;
}
</style>
