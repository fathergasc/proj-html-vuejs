<template>
  <div class="doctor-card">
    <img :src="getImgPath(doctor.profilePic)" :alt="`Dr.${doctor.name}`">
    <div class="p-4">
        <span class="text-uppercase pb-1">{{doctor.name}}</span>
        <span>{{doctor.position}}</span>
        <p class="text-black-50 py-3">{{doctor.text}}</p>
        <div class="doctor-contacts">
            <div v-for="(contact, index) in doctor.socials" :key="index" :style="contact.color">
                <a :href="contact.link" v-html="contact.icon" target="_blank" rel="noopener noreferrer"></a>
            </div>
        </div>
    </div>
    
  </div>
</template>

<script>
export default {
    name: 'DoctorCard',
    props: {
        doctor: Object
    },
    methods: {
        getImgPath(path) {
        return require('../assets/images/' + path)
    }
    }
}
</script>

<style lang="scss">

.doctor-card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    margin: 1.5rem;
    background-color: white;

    img {
        width: 100%;
    }
    
    span {
        display: block;
    }

    p {
        font-size: 0.8rem;
    }
}

.doctor-contacts {
    display: flex;
    justify-content: flex-start;
    align-items: center;

    div {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 30px;
        width: 30px;
        margin-right: 1rem;
        border-radius: 5px;
    }
    
    i {
        color: white;
    }

    
}
    
</style>