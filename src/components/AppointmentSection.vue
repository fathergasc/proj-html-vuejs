<template>
    <section id="appointment">
        <SectionHeader :header="appointmentHeaderData"/>
        <form action="URL" method="POST">
            <input class="form_small" type="text" placeholder="Name*" required>
            <input class="form_small" type="email" placeholder="Email*" required>
            <input class="form_small" type="tel" placeholder="Phone Number*" required>
            <input class="form_small" type="date" required>
            <textarea class="form_big" name="text" cols="8" rows="6" placeholder="How can we help?*"></textarea>
            <span class="my_button btn_blue">make an appointment</span>
        </form>
    </section>
  
</template>

<script>
import SectionHeader from './SectionHeader.vue'

export default {
    components: {
        SectionHeader,
    },
    data() {
        return {
            appointmentHeaderData: {
            title: 'Make an Appointment',
            text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation',
        },
        }
        
    }
}
</script>

<style lang="scss">

@import '../styles/variables.scss';

#appointment {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url('../assets/images/make-an-appointment.jpg');
    background-size: cover;
    background-position: center;
    color: white;
    padding: 6rem 0;

    h2 {
        text-transform: capitalize;
    }
}

form {
    display: flex;
    flex-wrap: wrap;

    .form_small {
        width: calc(50% - 2rem);
        margin: 1rem;
        padding: 0.5rem;
        background-color: transparent;
        border: 1px solid $grey_light;
        color: grey;
    }

    .form_big {
        width: 100%;
        margin: 1rem;
        padding: 0.5rem;
        background-color: transparent;
        border: 1px solid $grey_light;
        
    }

    .my_button.btn_blue {
        margin: 1rem;
        width: 100%;
        text-align: center;
        padding: 0.5rem;
    }
}

input[type="date"] {
    color: grey;
}

</style>