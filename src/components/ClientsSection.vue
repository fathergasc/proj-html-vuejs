<template>
  <section id="clients">
    <div class="container">
        <a class="mx-4" :href="client.link" v-for="(client, index) in clients" :key="index"><img  :src="getImgPath(client.image)"></a>
    </div>
  </section>
</template>

<script>
export default {
 name: 'ClientsSection',
 data() {
    return {
        clients: [
            {
                image: 'client-logos-1.png',
                link: '#'
            },
            {
                image: 'client-logos-2.png',
                link: '#'
            },
            {
                image: 'client-logos-3.png',
                link: '#'
            },
            {
                image: 'client-logos-4.png',
                link: '#'
            },
        ]
    }
 },
 methods: {
    getImgPath(path) {
        return require('../assets/images/' + path)
    } 
 },
}
</script>

<style scoped lang="scss">
@import '../styles/variables.scss';

#clients {
    display: flex;
    align-items: center;
    background-image: linear-gradient(90deg, $blue_light, $blue_median, $blue_dark);
}

.container {
    flex-direction: row;
    align-items: center;
    justify-content: center;

    
}

</style>