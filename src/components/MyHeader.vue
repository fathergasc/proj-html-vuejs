<template>
  <header>
    <div id="nav-bar">
        <a href="#"><img src="../assets/images/medical_logo_1x_light.png" alt=""></a>
        <div id="nav-bar-right">
            <!-- navbar links -->
            <ul>
                <li v-for="(navItem, index) in navBarLinks" :key="index"><a :href="navItem.link" class="ms-1 p-3">{{navItem.name}}</a></li>
            </ul>
            <a href="#appointment" class="ms-4 my_button btn_blue">Make appointment</a>
        </div>
    </div>
    <!-- jumbotron -->
    <div id="header-card" class="container d-flex align-items-start flex-column justify-content-center">
        <h1>Caring <span>For Life</span></h1>
        <p class="py-2">Kind words can be short and easy to spaek, but thei echoes are truly endless. Avada Health focuses on you as if it was our own family.</p>
        <a href="#welcome" class="my_button btn_blue">learn more</a>
    </div>
  </header>
</template>

<script>
export default {
 name: 'MyHeader',
 data() {
  return {

    //data for navbar links v-for
   navBarLinks: [
    {
     name: 'Home',
     link: '#'
    },
    {
     name: 'About',
     link: '#welcome'
    },
    {
     name: 'Departments',
     link: '#services'
    },
    {
     name: 'Articles',
     link: '#'
    },
   ]
  }
 }
}
</script>

<style lang="scss">
// my custom scss
@import '../styles/variables.scss';
@import '../styles/common.scss';

header {
    width: 100%;
    height: 90vh;
    background-image: url(../assets/images/header-image-homepage.jpg);
    background-size: cover;
    background-position: top;
    position: relative;
}

#nav-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 6rem;
    padding: 1rem 3rem;
    font-size: 0.8rem;   
    position: absolute;
    top: 0;
    left: 0; 
    width: 100%;
}

#nav-bar-right {
    display: flex;
    justify-content: center;
    align-items: center;
    text-transform: uppercase;
    
    ul {
        display: flex;
        justify-content: center;
        align-items: center;

        a {
        color: white;
        }
    }
}

#header-card {
    width: 100%;
    height: 100%;
    margin: 0 auto;

    h1 {
        font-size: 4rem;
        color: white;
        font-weight: 200;

        span {
            color: $blue_light;
        }
    } 

    p {
        color: white;
        width: 60%;
    }
}
    


</style >