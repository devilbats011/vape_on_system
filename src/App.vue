<template>
  <v-app class="general-bg" >
    <v-app-bar
      style="color:white"
      fixed
      :elevation="0"
      color="#00000055"
      
      height="66"
    >
      <!-- <v-app-bar-nav-icon color="white"></v-app-bar-nav-icon> -->
      <v-toolbar-title class="mx-5"><router-link to="/">Home</router-link><br></v-toolbar-title>
      <v-toolbar-title class="mx-5"><router-link to="/checkout"> Products</router-link></v-toolbar-title>
        <v-toolbar-title class="mx-5">Reach Us</v-toolbar-title>
      <v-spacer></v-spacer>
      <router-link to="/checkout"> 
      <v-app-bar-nav-icon color="white" ></v-app-bar-nav-icon>
      </router-link>
      <v-toolbar-title class="mx-5">username</v-toolbar-title>

    </v-app-bar>

    <v-content>
       <router-view />
    </v-content>
    <v-footer
      app
      color="transparent"
      class="white--text"
      style="margin-bottom:1rem"
    >
      <span><small>vaperchill@email.com</small></span>
      <v-spacer></v-spacer>
      <span><small>&copy; 2020</small></span>
    </v-footer>
  </v-app>

</template>

<script>
// import HelloWorld from './components/HelloWorld';
// import Homey from './components/Homey';
export default {
  name: 'App',

  components: {
    // HelloWorld,
    // Homey
    
  },

  data(){
    return{
      cards: [
        { title: 'Vodoo Stix', src: 'voopoo.png' },
        { title: 'Vodoo Stix', src: 'voopoo.png'},
        { title: 'Vodoo Stix', src: 'voopoo.png'},
        { title: 'Vodoo Stix', src: 'voopoo.png'},
        { title: 'Vodoo Stix', src: 'voopoo.png'},
        { title: 'Vodoo Stix', src: 'voopoo.png'},
        { title: 'Vodoo Stix', src: 'voopoo.png'},
        { title: 'Vodoo Stix', src: 'voopoo.png'},

        // { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },

      ],
    }
  },
};
</script>
<style>
  a
  {
    text-decoration: none;
  }
  a.router-link-active
  {
    text-shadow: 0 0 3px blue !important;
  }

  .clip-polygon {
  clip-path: polygon(0 0, 28% 0, 72.2% 100%, 0% 100%);
  opacity: 0.5;
  height:100%;width:100%;
  position:absolute;
  background:black;
  }

  .clip-polygon2{
    /* clip-path:polygon(100% 0%, 34% 0%, 78% 100%, 100% 100%); */
    opacity: 0.7;
    /* z-index: 2px; */
    height:100%;width:100%;
    position:absolute;
    background:black;
  }

  

  .show-products-container{
    position:relative;
    background:#5d5e60;
    height:auto;
    border-radius: 4px;
    margin:auto;
    width:74%;
    padding:2rem 0;

  }


  .products-content
  {
    /* border:1px solid red; */
    min-height:200px;
    width:99%;
    margin:auto;
    display:flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: flex-start;
    padding-left:8.6%;

  }
/* each  div is 28 can fill up 3 space  ,total space : 84%,remaining 16%;putting padding 8 left and the right  it bee */
    .products-content > div{
    margin:1%;
    width:28%;
    height:260px;
    border:0px solid grey;
    position:relative;
    border-radius: 4px;
  }

      .main-container{
        margin:5rem auto;
        color:white;
    }

    .main-content{
            position:relative;
    /* background:#5d5e60; */
    /* background-image: url(./assets/v2.jpg); */
    border: 1px solid red;
    background-position: center;
    background-size: cover;
    border-radius: 4px;
    margin:auto;
    width:86%;
    min-height:500px;
    }

  .contact-container{
    position:relative;
    /* background:#5d5e60; */
    /* background-image: url(./assets/v2.jpg); */
    border: 1px solid black;
    background-position: center;
    background-size: cover;
    border-radius: 4px;
    margin:auto;
    width:86%;
    min-height:500px;
    /* text-align: center; */

  }

  .contact-content{
    position:relative;
    z-index:2;
    margin:auto;
    padding:2rem;
    width:80%;
    height:100%;
    /* border:0px solid red; */
    display:flex;
    flex-direction:column;
    justify-content: flex-start;
    align-items: center;
    
  }

  .sub-contact{
    position: relative;
    height:22%;
    width:65%;
    /* border:1px solid #060606; */
    /* background:#272727; */
    padding:1rem;
    margin-bottom:1rem;
  }

  .sub-contact > *
  {
    position: relative;
    z-index:2;

  }

  .sub-contact::before{
    content:'';
    position: absolute;
    top:0px;
    left:0px;
    height:100%;
    width:100%;
    z-index:0;
    opacity: 0.7;
    z-index: 1;
    /* border:1px solid #272727eb; */
    background:#060606;
  }

  .slider-btn-container
  {
    margin-left: -0.3rem;
    position: relative;
    top:1rem;
  }
  .slider-btn
  {
      border-radius:50%;border:2px solid white;height:13px;width:12px;
      /*margin: y,x */
      margin:0rem 0.4rem; 
      transition: 0.6s;

 
  }
  .active-slider-btn{
        border-radius:0% !important;
         transform: rotate(45deg);
        height:13px;width:13px;
         border:2px solid grey;
         margin:0 0.4rem !important;
         background: #ffffff;

    }     
  .general-bg
  {
    background:#16161a !important;
  }
  .grad{
    position:absolute;
    bottom:0px;left:0px;
    height:30%;
    width:100%;
  }

  .grad::before{
    /* background: linear-gradient(0deg, rgba(22,22,26,1) 5%, rgba(22,22,26,1) 10%, rgba(22,22,26,0.6362920168067228) 5%, rgba(22,22,26,0.006039915966386533) 10%); */
    content:"";
    background:black !important;
    opacity: 0.8;
    position: absolute;
    width: 100%;
    height: 100%;
  }
    
    .b-ground{
/* background:transparent; */
background:linear-gradient(0deg, rgba(22,22,26,1) 97%, rgba(22,22,26,1) 0%, rgba(22,22,26,26.636292) 96%, rgba(22,22,26,0.006039915966386533) 100%);
    }
 
</style>