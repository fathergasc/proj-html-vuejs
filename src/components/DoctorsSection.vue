<template>
    <section id="doctors">
        <div class="container">
            <SectionHeader :header="doctorsHeaderData" />
            <div id="doctors-card">
                <DoctorCard v-for="(doctor, index) in doctorsData" :key="index" :doctor="doctor" />
            </div>
        </div>
    </section>
</template>

<script>
import SectionHeader from "./SectionHeader.vue";
import DoctorCard from "./DoctorCard.vue";

export default {
    name: "DoctorsSection",
    components: {
        SectionHeader,
        DoctorCard,
    },
    data() {
        return {
            //data for section header
            doctorsHeaderData: {
                icon: "icon-5.png",
                title: "meet our doctors",
                text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation",
            },
            //data for doctors card v-for
            doctorsData: [
                {
                    profilePic: "doctor-1.jpg",
                    name: "Jon Snow",
                    position: "Anesthesiologist",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt",
                    socials: [
                        {
                            icon: '<i class="fa-brands fa-facebook-f"></i>',
                            link: "https://www.facebook.com/",
                            color: "background-color: #3c5998",
                        },
                        {
                            icon: '<i class="fa-brands fa-twitter"></i>',
                            link: "https://twitter.com/",
                            color: "background-color: #54acee",
                        },
                        {
                            icon: '<i class="fa-brands fa-instagram"></i>',
                            link: "https://www.instagram.com/",
                            color: "background-color: #3f729b",
                        },
                    ],
                },
                {
                    profilePic: "doctor-2.jpg",
                    name: "Tony Stark",
                    position: "Cardiologist",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt",
                    socials: [
                        {
                            icon: '<i class="fa-brands fa-facebook-f"></i>',
                            link: "https://www.facebook.com/",
                            color: "background-color: #3c5998",
                        },
                        {
                            icon: '<i class="fa-brands fa-twitter"></i>',
                            link: "https://twitter.com/",
                            color: "background-color: #54acee",
                        },
                        {
                            icon: '<i class="fa-brands fa-instagram"></i>',
                            link: "https://www.instagram.com/",
                            color: "background-color: #3f729b",
                        },
                    ],
                },
                {
                    profilePic: "doctor-3.jpg",
                    name: "Anna Smith",
                    position: "Nurse Practitioner",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt",
                    socials: [
                        {
                            icon: '<i class="fa-brands fa-facebook-f"></i>',
                            link: "https://www.facebook.com/",
                            color: "background-color: #3c5998",
                        },
                        {
                            icon: '<i class="fa-brands fa-twitter"></i>',
                            link: "https://twitter.com/",
                            color: "background-color: #54acee",
                        },
                        {
                            icon: '<i class="fa-brands fa-instagram"></i>',
                            link: "https://www.instagram.com/",
                            color: "background-color: #3f729b",
                        },
                    ],
                },
            ],
        };
    },
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

#doctors {
    background-color: $grey_light;
}

#doctors-card {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
