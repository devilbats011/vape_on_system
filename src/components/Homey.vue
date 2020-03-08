<template>
<main>
         <v-img src="../assets/v5.jpg"
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
            v-bind:src="require('../assets/products/' + card.src)" 
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
            <v-img class="contact-container" src="../assets/v2.jpg" >
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


</main>


</template>

<script>
export default {
    name:"Homey",
    data(){
        return {
            img:"./assets/v5.jpg",
            cards: [
                { title: 'Vodoo Stix', src: 'voopoo.png' },
                { title: 'Vodoo Stix', src: 'voopoo.png'},
                { title: 'Vodoo Stix', src: 'voopoo.png'},
                { title: 'Vodoo Stix', src: 'voopoo.png'},
                { title: 'Vodoo Stix', src: 'voopoo.png'},
                { title: 'Vodoo Stix', src: 'voopoo.png'},
                { title: 'Vodoo Stix', src: 'voopoo.png'},
                { title: 'Vodoo Stix', src: 'voopoo.png'},
            ],
    
        }
    }

}
</script>

<style>

</style>