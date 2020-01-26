<template>
<div id="app">
  <v-app id="inspire">

      
    <v-app-bar
      style="color:white"
      fixed
      :elevation="0"
      scroll-target="#scrolling-techniques-7"
      color="transparent"
      height="66"
    >
      <v-app-bar-nav-icon color="white"></v-app-bar-nav-icon>
      <v-toolbar-title>Toolbar</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon color="white" @click.stop="drawerRight = !drawerRight"></v-app-bar-nav-icon>
    </v-app-bar>
    <!-- <div
       style="background:#16161a;height:66px;width:100%;margin:0px"
              >
    </div> -->
       <v-img src="./assets/v5.jpg"
        style="height:650px;width:100%;margin:0px;" cover 
       ></v-img>

    <v-content style="margin-top:-148px" >
      <v-sheet color="transparent" style="height:1500px;padding-top:10.5rem;color:white" class="b-ground" justify-center >
        <v-container>
            <h2>Wht Up!</h2>
        </v-container>
        
      </v-sheet>
    </v-content>

    <v-footer
      app
      color="#16161a"
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
  name: 'App',

  components: {

  },

  data: () => ({
    //
  }),
};
</script>

<style>
  
  .general-bg
  {
    background-color:#16161a;
  }
    
    .b-ground{

background:transparent;
background: linear-gradient(0deg, rgba(22,22,26,1) 0%, rgba(22,22,26,1) 90%, rgba(22,22,26,0.6362920168067228) 95%, rgba(22,22,26,0.006039915966386533) 100%);
    }
 
</style>
