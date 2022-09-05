<template>
<div class="container">
    <div class="section-header">
        <img :src="getImgPath(header.icon)" alt="">
        <h2 class="py-3">{{header.title}}</h2>
        <p>{{header.text}}</p>
    </div>
</div>
  
</template>

<script>
export default {
 name: 'SectionHeader',
 props: {
    header: Object
 },
 methods: {
    getImgPath(path) {
        return require('../assets/images/' + path)
    } 
 },
}
</script>

<style lang="scss">
@import '../styles/variables.scss';

.section-header {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 60%;
    text-align: center;

    img {
        width: $icon_width;
    }

    h2 {
        text-transform: uppercase;
        font-size: 1.5rem;
    }
}

</style>