<template>
<div class="container">
 <div class="header">
        <a href="#">
          <img  class="logo" src="../assets/img/NT.svg"  alt="logo" />
        </a>

        
        <div class="align-center d-flex">
          <a href="#">
            <img
              src="@/assets/img/search.svg"
              class="search-icon"
              alt="Search"
               width ="20"
            />
          </a>
          <button
            id="menu"
            @click="openNav()"
            class="slide_from_left"
            title="Menu"
          >
            Menu
          </button>
         
        </div>
 </div>
<div id="mySidenav" ref="sidenav" class="sidenav">
    <a href="javascript:void(0)" class="closebtn" @click="closeNav()">&times;</a>
  <ul>
   
    <li>
        <a href="#">About Us</a>
    </li>
      <li>
        <a href="#">Pick your Trip</a>
    </li>
      <li>
         <a href="#">Join Us</a>
    </li>
      <li>
        <a href="#">Contact Us</a>
    </li>
  </ul>
</div>

</div>
</template>
<script>
export default {
  props: [],
  data() {
    return {};
  },
  methods: {
    openNav(){
    var vm = this;
    vm.$refs.sidenav.style.width= "100%";
  },
   closeNav(){
    var vm = this;
    vm.$refs.sidenav.style.width= "0";
  }
  },
};
</script>

<style lang="scss">
@import "../assets/scss/header";
</style>
