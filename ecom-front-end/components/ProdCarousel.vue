<template>
<div class="uk-section uk-section-muted uk-margin-top uk-padding-remove-bottom">
<div class="uk-container uk-container-xlarge">
<VueSlickCarousel v-bind="slickOptions">
      <div v-for="i in 5" :key="i" class="img-wrapper">
        <img :src="`./${i}-slider.jpg`" />
      </div>
</VueSlickCarousel>
</div>
</div>
</template>
<script>
export default {
data() {
    return {
      slickOptions: {
        slidesToShow: 3,
        arrows: false
      }
    }
  }
}
</script>
<style scoped>
.img-wrapper img {
 border: solid 2px red;
  margin: auto;
  width: 924px;
  height: 470px;
  background: #000;
}
</style>
   