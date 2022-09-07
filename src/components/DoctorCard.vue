<template>
    <div class="doctor-card">
        <img :src="getImgPath(doctor.profilePic)" :alt="`Dr.${doctor.name}`" />
        <div class="p-4">
            <span class="text-uppercase pb-1 dark-text">{{ doctor.name }}</span>
            <span class="dark-text">{{ doctor.position }}</span>
            <p class="grey-text py-3">{{ doctor.text }}</p>
            <div class="doctor-contacts">
                <!-- prints social link with brand color ad bg-color of the element -->
                <SocialLink :contact="contact" v-for="(contact, index) in doctor.socials" :key="index" />
            </div>
        </div>
    </div>
</template>

<script>
import SocialLink from "./SocialLink.vue";

export default {
    name: "DoctorCard",
    props: {
        doctor: Object,
    },
    components: {
        SocialLink,
    },
    methods: {
        getImgPath(path) {
            return require("../assets/images/" + path);
        },
    },
};
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
        font-size: 0.9rem;
    }
}

.doctor-contacts {
    display: flex;
    justify-content: flex-start;
    align-items: center;
}
</style>
