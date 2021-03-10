<template>
<div>
  <div class="tabs-Info">
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
</template>
<script>
export default {
  props: ["TabItem", "Title", "Description", "tabDescription"],
  data() {
    return {
      active: 0,
    };
  },
  methods: {
    change: function (num) {
      this.active = num;
    },
  },
  created() {
  },
};
</script>