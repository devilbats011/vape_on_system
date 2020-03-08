<template >
<div id="app" class="general-bg">
  <v-app id="inspire" class="general-bg">

    <v-app-bar
      style="color:white"
      fixed
      :elevation="0"
      color="transparent"
      height="66"
    >
      <!-- <v-app-bar-nav-icon color="white"></v-app-bar-nav-icon> -->
      <v-toolbar-title class="mx-5">Home</v-toolbar-title>
      <v-toolbar-title class="mx-5">Products</v-toolbar-title>
        <v-toolbar-title class="mx-5">Reach Us</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon color="white" @click.stop="drawerRight = !drawerRight"></v-app-bar-nav-icon>
      <v-toolbar-title class="mx-5">username</v-toolbar-title>

    </v-app-bar>
    <!-- <div
       style="background:#16161a;height:66px;width:100%;margin:0px"
              >
    </div> -->
       <v-img src="./assets/v5.jpg"
        style="height:680px;width:100%;margin:0px;" cover 
       >

          <div style="position:absolute;font-size:1.1rem;bottom:47%;right:0;border:0px solid black;width:45%;margin:0 0.3rem"  class=" d-flex flex-column" >
                    <p style="color:#fff;max-width:530px;font-size:1.1rem;" >
                      It is a long established fact that a reader will be distracted by the readable content of a page
                      when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal 
                      distribution of letters, as opposed to using 'Content here, content here', making it look like 
                      readable English.
                    </p>
              <seciton class="slider-btn-container mt-3">
                 <button class="slider-btn active-slider-btn"> </button>
                  <button class="slider-btn"> </button>
                  <button class="slider-btn"> </button>
                  <button class="slider-btn"> </button>
                  <button class="slider-btn"> </button>
                  <button class="slider-btn"> </button>
              </seciton>
              </div>
       </v-img>

    <v-content style="margin-top:-148px" >
      <v-sheet color="transparent" style="height:auto;color:white;position:relative;top:1.4rem;" class="b-ground" justify-center >
        <v-container class="" style="position:relative;top:-3.8rem;margin:1.8rem auto;">
        <v-row>
        <v-col :cols="6">
          <v-card
            color="transparent"
            style="color:white;text-align:right;padding-right: 0rem;"
            outlined  
          >
        <span style="font-size:2rem;"> <b><u> Contact Watsapps</u> </b></span>
          </v-card>
        </v-col>

        <v-col :cols="6" >
          <v-card
            color="transparent"
            style="color:white;text-align:left;padding-left: 2.4rem;"
            outlined  
          >
        <span style="font-size:2rem;"> <b><u> Login Facebook</u> </b></span>
          </v-card>
        </v-col>

      </v-row>
        </v-container>

        <main class="show-products-container" >
          
          <!-- margin:auto is to balance between left and right so the element section will be center! -->
          <!-- cant push margin like margin:1rem auto(this will not work) because
           the parent element height is auto ,need to use padding to push ,eg :padding 1rem 0;-->
          <section class="products-content">
          <div
          v-for="card in cards"
          :key="card.title"
          style=""
          >
          <img  style="background:transparent;position:absoulte;width:100%;background-position:center;border-radius:2px;" height="100%"
            v-bind:src="require('./assets/products/' + card.src)" 
          >
          <article class="grad">
            <div style="position:relative;z-index:2;padding:0.4rem;">
              <p>{{card.title}}</p>

            </div>
          </article>
          </div> 
          </section>
        </main>
        <br><br>
        <v-container class="white--text" style="position:relative;margin-bottom:3rem;" >
            <v-img class="contact-container" src="./assets/v2.jpg" >
              <!-- <img class="clip-polygon" /> -->
              <img class="clip-polygon2" />
              <div class="contact-content" >
             
                  <br>
                  <article><h1>C o n t a c t<hr></h1></article>
                  <br>
                  <article class="sub-contact" >
                    <p>Name</p>
                    <p>Parker Bark</p>
                  </article>

                  <article class="sub-contact">
                    <p>Email</p>
                    <p>Parker Bark</p>
                  </article>

                 <article class="sub-contact" >
                    <p>Message</p>
                    <p>Parker Bark</p>
                  </article>
                <!-- <article class="" style="height:100px;background:red;width:100px;" >
                  wefwef  
                  </article> -->

              </div>

              
            </v-img>
        </v-container>
        
      </v-sheet>
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
</div>
</template>

<script>

export default {
  name: 'Home',
  components: {

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
