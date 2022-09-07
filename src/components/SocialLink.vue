<template>
    <div class="socials-link-wrapper">
        <div class="social-link" :style="contact.color">
            <a :href="contact.link" v-html="contact.icon" target="_blank" rel="noopener noreferrer"></a>
        </div>
    </div>
</template>

<script>
export default {
    name: "SocialLink",
    props: {
        contact: Object,
    },
};
</script>

<style lang="scss">
.social-link {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 30px;
    width: 30px;
    margin-right: 1rem;
    border-radius: 5px;

    a {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    i {
        color: white;
    }
}
</style>
