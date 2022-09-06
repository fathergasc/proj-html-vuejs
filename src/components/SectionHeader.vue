<template>
    <div class="section-header">
        <img v-if="header.hasOwnProperty('icon')" class="pt-1" :src="getImgPath(header.icon)" alt="">
        <h2 class="py-5">{{header.title}}</h2>
        <p>{{header.text}}</p>
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
        font-size: 1.8rem;
        position: relative;
        font-weight: 300;
        
        &::after {
            content: '';
            display: block;
            width: 200px;
            height: 1px;
            background-color: lighten($grey_dark, 30%);
            position: absolute;
            left: 50%;
            bottom: 20%;
            transform: translate(-50%, 0);

        }
    }
}

</style>