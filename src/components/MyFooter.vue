<template>
  <footer id="footer">
    <div class="footer-top">
        <div class="footer-top-left">
            <img src="../assets/images/medical_logo_1x_dark.png" alt="">
            <p class="text-black-50">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque natus dignissimos aliquid ducimus. Nam nostrum illum, ullam exercitationem error dolorem.</p>
            <span class="text-uppercase">learn more about us</span>
            <div class="d-flex justify-content-start py-4">
                <!-- prints social link with brand color ad bg-color of the element -->
                <SocialLink :contact="contact" v-for="(contact, index) in socials" :key="index"/>
            </div>
        </div>
        <div class="footer-top-center">
            <FooterList :contacts="contactsInfo"/>
        </div>
        <div class="footer-top-right">
            <FooterList :contacts="departmentsInfo" class="pb-5"/>
            <span class="my_button btn_white my-3"><a href="#" >view our departments</a></span>
        </div>
    </div>
    <div class="footer-bot">
        <span>&#169; Copyright 2012 - 2022 | Avada Theme by <a href="#">ThemeFusion</a> | All Rights Reserved | Powered by <a href="#">WordPress</a></span>
        <a href="#" class="back-top"><i class="fa-solid fa-chevron-up"></i></a>
    </div>
  </footer>
</template>

<script>
import FooterList from './FooterList.vue'
import SocialLink from './SocialLink.vue'

export default {
    name: 'MyFooter',
    components: {
        FooterList,
        SocialLink
    },
    data() {
        return {
            //data for socials links v-for in .footer-top-left
            socials: [
                        {
                            icon: '<i class="fa-brands fa-facebook-f"></i>',
                            link: 'https://www.facebook.com/',
                            color: 'background-color: #3c5998'
                        },
                        {
                            icon: '<i class="fa-brands fa-twitter"></i>',
                            link: 'https://twitter.com/',
                            color: 'background-color: #54acee'
                        },
                        {
                            icon: '<i class="fa-brands fa-youtube"></i>',
                            link: 'https://www.youtube.com/',
                            color: 'background-color: #cd201f'
                        },
                        {
                            icon: '<i class="fa-brands fa-instagram"></i>',
                            link: 'https://www.instagram.com/',
                            color: 'background-color: #3f729b'
                        },
                    ],
            //data for ul in .footer-top-center        
            contactsInfo: [
                {
                    title: 'contact information',
                    items: [
                        {
                            icon: '<i class="fa-solid fa-location-dot"></i>',
                            text: '121 King Street, London United Kingdom'
                        },
                        {
                            icon: '<i class="fa-solid fa-phone-flip"></i>',
                            text: '1.800.458.556'
                        }
                    ]
                }
            ],
            //data for ul in .footer-top-right
            departmentsInfo: [
                {
                    title: 'medical departments',
                    items: [
                        {
                            icon: '<i class="fa-solid fa-chevron-right"></i>',
                            text: 'Cardiology',
                            link: '#'
                        },
                        {
                            icon: '<i class="fa-solid fa-chevron-right"></i>',
                            text: 'Pediatrics',
                            link: '#'
                        },
                        {
                            icon: '<i class="fa-solid fa-chevron-right"></i>',
                            text: 'Diabetes Care',
                            link: '#'
                        },
                        {
                            icon: '<i class="fa-solid fa-chevron-right"></i>',
                            text: 'Pre-natal Care',
                            link: '#'
                        },
                        {
                            icon: '<i class="fa-solid fa-chevron-right"></i>',
                            text: 'Ultrasound Echocardiogram',
                            link: '#'
                        },
                    ]
                }
            ],
        }
    }
}
</script>

<style lang="scss">

@import '../styles/variables.scss';

#footer {
    width: 100%;
    padding-top: 3rem;
}

.footer-top {
    display: flex;
}

.footer-top-left, .footer-top-center, .footer-top-right {
    width: calc(100% / 3);
    padding: 2rem;
}

.footer-top-left {

    p {
        border-bottom: 1px solid lighten($grey_dark, 30%);
        padding: 1rem 0;
        font-weight: 400;
    }
}

.footer-top-right {

    li:hover > a {
        color: $blue_light
    }

    i {
        width: 30px;
        height: 30px;
        line-height: 30px;
        text-align: center;
        border-radius: 50%;
        color: white;
        background-color: $blue_light;
    }
}

.footer-bot {
    background-color: $grey_light;
    height: 4rem;
    width: 100%;
    margin-top: 3rem;
    color: $grey_dark;
    font-size: 0.8rem;
    display: flex;
    align-items: center;
    padding-left: 2rem;
    position: relative;

    a {
        color: black;

        &:hover {
            color: $blue_light;
        }
    }

    .back-top {
        position: absolute;
        bottom: 0;
        border-radius: 5px 5px 0 0;
        right: 2rem;
        width: 30px;
        height: 30px;
        background-color: $grey_median;
        color: white;
        display: flex;
        align-items: center;
        justify-content: center;

        &:hover {
            color: white;
        }
    }
}

</style>