<template>
  <div class="small-card">
    <img :src="getImgPath(card.image)" alt="">
    <h5 class="py-3">{{card.title}}</h5>
    <p class="text-black-50">{{card.text}}</p>
  </div>
</template>

<script>
export default {
 name: 'SmallCard',
 props: {
    card: Object
 },
 methods: {
    getImgPath(path) {
        return require('../assets/images/' + path)
    }
 }
}
</script>

<style lang="scss">
@import '../styles/variables.scss';

.small-card{
    text-align: center;
    font-weight: 300;

    img {
        width: $icon_width;
    }

    h5 {
        font-size: 0.9rem;
        text-transform: uppercase;
        font-weight: 400;
    }

    p {
        font-size: 0.8rem;
    }
}

</style>