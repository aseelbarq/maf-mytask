<template>
<div>
  <div>
    <div class="tabs">
      <ul class="d-flex">
        <li
          v-for="(tab, index) in tabItem"
          v-bind:key="tab.id"
          :class="{ 'active': show == index }"
        >
          <a @click.prevent="show = index">{{ tab.Title }}</a>
        </li>
      </ul>
    </div>
    <div class="tabs-content">
      <section @click.native="Move($event);">
      <div v-for="(tab, index) in tabItem"  :key="index">
        <div v-if="show == index">
          <div>
  <div class="Tabs">
    <div   v-for="(Tab, index) in TabItem" :key="index">
    <div
      class="image-tab"
    
      v-if="active == index"
    >
      <div class="img-section">
        <img class="fade-in" src="@/assets/img/desert.svg" srcset="" alt="desrt-image"  />
      </div>
      <div class="tabs-desc">
        <div class="number">{{ Tab.num }}</div>
        <div class="title">{{ Tab.title }}</div>
      </div>
     
    </div>
  </div>
    <div class="text-tab">
      <div class="title">
        {{ Title }}
      </div>
      <div class="description">
        <div>{{ Description }}</div>
        <div>{{ tabDescription }}</div>
        
      </div>
      
    </div>
  </div>

</div>
            <TabsContentComponent :TabItem="tab.Image" :tabDescription="tab.Description" :Title="tab.Title"/>
        </div>
      </div>
      </section>
    </div>
  </div>

    <section class="footer">
<div class="social-media-share">share it</div>
 <div class="social-media">
    <a href="#" title="instagram" target="_blank">
          <img
            width="20px"
            src="@/assets/img/instagram.svg"
            alt="instagram"
          />
        </a>
         <a href="#" title="twitter" target="_blank">
          <img  src="@/assets/img/twitter.svg" alt="twitter" />
        </a>
        <a href="#" target="_blank" title="facebook">
          <img src="@/assets/img/facebook.svg" alt="facebook" />
        </a>
       
       
      </div>

</section>
</div>
</template>

<script>
import TabsContentComponent from "./TabsContentComponent";

export default {
  props: ["tabItem"],
  components: {
    TabsContentComponent,
  },
  data() {
    return {
      show: 0,
    };
  },
  methods: {
   
  }
};
</script>