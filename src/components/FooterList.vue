<template>
  <div class="footer-list">
    <h5 class="text-uppercase">{{contacts[0].title}}</h5>
    <ul>
        <li v-for="(contact, index) in contacts[0].items" :key="index" ><a :href="contact.link" v-html="contact.icon + contact.text"></a>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
 name: 'FooterList',
 props: {
    contacts: Array
 }
}
</script>

<style lang="scss">

@import '../styles/variables.scss';

.footer-list {
    text-align: left;

    h5 {
        font-weight: 400;
        margin-bottom: 2rem;

        &::after {
            content: '';
            display: block;
            width: 50px;
            height: 2px;
            background-color: $blue_light;
            margin: 2rem 0;
        }
    }

    i {
        margin-right: 10px;
        color: $blue_light;
    }

    li {
        margin: 1rem 0;
        
        a {
            color: grey;
        }
    }
}

</style>