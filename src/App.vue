<script>
import Main from './components/Main.vue';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
export default {

  components: {
    AppHeader,
    Main,
    AppFooter,
  },
  data() {
    return {
      
    }
  },
  methods: {
    
  
  },
  mounted() {
    
  }
}
</script>

<template>
  <div class="menu">

<div class="item first">
  <span class="label"><i class="fa-regular fa-newspaper"></i></span>
  <span class="tooltip">
    <span class="contenitoreTesto">Select Demo</span>
    <span class="triangle first"></span>
  </span>
</div> 

<div class="item second">
  <span class="label"><i class="fa-regular fa-comment"></i></span>
  <span class="tooltip">
    <span class="contenitoreTesto">Support Channel</span>
    <span class="triangle second"></span>
  </span>
</div>

<div class="item third">
  <span class="label"><i class="fa-regular fa-rectangle-list"></i></span>
  <span class="tooltip">
    <span class="contenitoreTesto">Documentation</span>
    <span class="triangle third"></span>
  </span>
</div>

<div class="item fourth">
  <span class="label"><i class="fa-regular fa-credit-card"></i></span>
  <span class="tooltip">
    <span class="contenitoreTesto">Purchase</span>
    <span class="triangle fourth"></span>
  </span>
</div>
</div>

  <AppHeader />
  <Main></Main>
  <AppFooter />
    
</template>

<style scoped>
  .menu {
  position: fixed;
  top: 200px;
  right: 0;
  z-index: 999;
  background-color: #F5F5F5;
  border-radius: 10px;
  padding: 20px 10px;
  box-shadow: 0px 0px 4px 2px rgba(0,0,0,0.5);
}
.item{
  position: relative;
  cursor: pointer;
  color: #333333;
  padding: 4px 0;
}
.tooltip {
  display: none;
  position: fixed;
  right: 50px;
  padding: 5px;
  border-radius: 4px;
  font-size: 12px;
}
.contenitoreTesto {
  display: inline-block;
  padding: 2px 10px;
  background-color: #F5F5F5;
  border-radius: 5px;
  position: relative;
  z-index: 800;
}
.triangle {
  background-color: #F5F5F5;
  display: inline-block;
  height: 5px;
  width: 10px;
  transform: rotate(45deg);
  position: absolute;
  top: 30%;
  right: 1px;
  z-index: 1;
}
.first > .tooltip {
  top: 220px;
}
.second > .tooltip {
  top: 245px;
}
.third > .tooltip {
  top: 270px;
}
.fourth > .tooltip {
  top: 295px;
}
.menu > .item:hover .tooltip {
  display: block;
}
.label>i{
  transition: all 0.2s ease-in-out;
}
.label>i:hover{
  color: #EF6F31;
}

</style>