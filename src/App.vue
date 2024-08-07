<script setup>
import { ref } from "vue";
import NavItem from "@/components/NavItem.vue";
import ShopDrop from "@/components/ShopDrop.vue";

const imageBg=ref("url(/toa-large.jpg) center/100% auto no-repeat")
const scrollOneColor = ref("hsl(0, 0%, 100%)");
const scrollTwoColor = ref("transparent");
const scrollThreeColor = ref("transparent");

let attributeIndex = 0;
const attributes = [
  { scrollOneColor: "hsl(0, 0%, 100%)", scrollTwoColor: "transparent", scrollThreeColor: "transparent" },
  { scrollOneColor: "transparent", scrollTwoColor: "hsl(0, 0%, 100%)", scrollThreeColor: "transparent" },
  { scrollOneColor: "transparent", scrollTwoColor: "transparent", scrollThreeColor: "hsl(0, 0%, 100%)" },
];

setInterval(() => {
  attributeIndex = (attributeIndex + 1) % attributes.length;
  const currentAttribute = attributes[attributeIndex];
  scrollOneColor.value = currentAttribute.scrollOneColor;
  scrollTwoColor.value = currentAttribute.scrollTwoColor;
  scrollThreeColor.value = currentAttribute.scrollThreeColor;

  if (scrollTwoColor.value == "hsl(0, 0%, 100%)") {
    imageBg.value = "url(/clark-large.jpg) center/100% auto no-repeat";
  }
  else if (scrollThreeColor.value == "hsl(0, 0%, 100%)") {
    imageBg.value = "url(/blake-large.jpg) center/100% auto no-repeat";
  }
  else{
    imageBg.value = "url(/toa-large.jpg) center/100% auto no-repeat";
  }
}, 5000);
</script>

<style scoped>
.bg-img{
  position:fixed;
  z-index:-1;
  width:100%;
  height:100%;
}
header{
  display:flex;
  flex-direction:row;
  justify-content:space-between;
  background-color: hsla(0, 0%, 8%, 0.747);
  padding:1vh 5vw;
}
.logo-ctn{
  width:4vw;
  height:4vh;
}
.logo-ctn img{
  width:100%;
  height:100%;
}
.shop-drop{
  margin: auto 0;
  display:none;
}
.nav-item{
  margin: auto 0;
}

@media screen and (max-width:750px){
  .logo-ctn {
    width: 40px;
    height: 40px;
  }
  .bg-img {
    transform:scale(2);
  }
  .nav-item{
    display:none;
  }
  .shop-drop{
    display:block;
  }
}


.scroll-level{
  position:absolute;
  bottom:0;
  width:100%;
  height:6vh;
  display:flex;
  place-items:center;
  justify-content:center;
}
.scroll-level-main{
  background-color: black;
  width:50%;
  height:2px;
  display:flex;
  flex-direction:row;
}
.scroll-level-main .one, .scroll-level-main .two, .scroll-level-main .three{
  width:33.33%;
  height:100%;
}
</style>

<template>
  <div class="bg-img" :style="{ background: imageBg }">
  </div>
  <div class="app-content">
    <header>
      <div class="content">
        <div class="logo-ctn">
          <img src="/public/Chel logo.svg" alt="">
        </div>
      </div>

      <div class="shop-drop">
        <ShopDrop />
      </div>

      <div class="nav-item">
        <NavItem />
      </div>

      <div class="nav-icon">

      </div>
    </header>
    <main></main>
    <div class="scroll-level">
      <div class="scroll-level-main">
        <div class="one" :style="{ backgroundColor: scrollOneColor }"></div>
        <div class="two" :style="{ backgroundColor: scrollTwoColor }"></div>
        <div class="three" :style="{ backgroundColor: scrollThreeColor }"></div>
      </div>
    </div>
  </div>
</template>


