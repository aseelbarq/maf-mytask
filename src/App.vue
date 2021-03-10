<template>
  <div id="app">
    <div class="bg-trip">
      <HeaderComponent/>
      <TripsComponent/>
      <SocialMediaComponent/>
      <TabsComponent  :tabItem="tabs" />
      <TabsContentComponent/>
     
     
      </div>

 
 
  </div>
</template>
<script>
import Data from './Data.json';
 import HeaderComponent from "./components/HeaderComponent";
import TripsComponent from "./components/TripsComponent";
import SocialMediaComponent from "./components/SocialMediaComponent";
import TabsComponent from "./components/TabsComponent";
import TabsContentComponent from "./components/TabsContentComponent";




export default {
  name: "App",
  data() {
     return {
        tabs: Data
    };
  },
  components: {HeaderComponent,TripsComponent,SocialMediaComponent ,TabsComponent,TabsContentComponent},
  methods: {
   
  },

};
</script>
<style lang="scss">
@import "./assets/scss/common";
</style>

 