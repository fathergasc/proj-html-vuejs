<template>
    <div class="learn-more-card">
        <h6>{{ card.title }}</h6>
        <img class="py-2" src="../assets/images/wave-divider.png" />
        <p class="py-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio, eligendi? Fugiat tempora delectus nulla ipsam facere sunt laboriosam</p>
        <span class="my_button btn_transparent">learn more</span>
    </div>
</template>

<script>
export default {
    name: "LearnMoreCard",
    props: {
        card: Object,
    },
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

.learn-more-card {
    width: calc(100% / 3);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 3rem;
    color: white;
    text-align: center;
}
</style>
