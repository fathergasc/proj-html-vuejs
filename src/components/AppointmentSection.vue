<template>
    <section id="appointment">
        <div class="container">
            <SectionHeader :header="appointmentHeaderData" />
            <form>
                <input class="form_small" type="text" placeholder="Name*" required />
                <input class="form_small" type="email" placeholder="Email*" required />
                <input class="form_small" type="tel" placeholder="Phone Number*" required />
                <!-- input type is text when not focused to allow the use of a placeholder and it's type date onfocus-->
                <input class="form_small" type="text" onfocus="type='date'" onfocusout="type='text'" placeholder="Appointment Date" required />
                <textarea class="form_big" name="text" cols="8" rows="6" placeholder="How can we help?*"></textarea>
                <input type="submit" class="my_button btn_blue" value="make an appointment" />
            </form>
        </div>
    </section>
</template>

<script>
import SectionHeader from "./SectionHeader.vue";

export default {
    components: {
        SectionHeader,
    },
    data() {
        return {
            datePlaceholder: "&#128198; Appointment Date",
            //data for section header
            appointmentHeaderData: {
                title: "Make an Appointment",
                text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation",
            },
        };
    },
};
</script>

<style lang="scss">
@import "../styles/variables.scss";

#appointment {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: url("../assets/images/make-an-appointment.jpg");
    background-size: cover;
    background-position: center;
    color: white;
    padding: 4rem 0;

    h2 {
        text-transform: capitalize;
    }

    .container {
        .section-header {
            h2,
            p {
                color: white;
            }
        }
    }
}

form {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 60%;

    input,
    textarea {
        font-weight: 500;
        color: white;
        font-size: 0.8rem;
    }

    .form_small {
        width: calc(50% - 2rem);
        margin: 1rem;
        padding: 0.5rem;
        background-color: transparent;
        border: 1px solid $grey_light;
        color: white;
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

// changes input type date calendar icon from black to white, to make it more visible on the background image of #appointment
input[type="date"]::-webkit-calendar-picker-indicator {
    filter: invert(1);
}
</style>
