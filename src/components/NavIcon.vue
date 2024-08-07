<script setup>
import { ref } from "vue";
import IconMenu from '@/components/IconMenu.vue';

const menuListDisplay = ref("none");
const menuIcon = ref("<i class='bx bxs-chevron-left'></i>");

const showIcons = () => {
    if (menuIcon.value == "<i class='bx bxs-chevron-left'></i>") {
        menuIcon.value = "<i class='bx bx-x'></i>";
        menuListDisplay.value = "flex";
    }
    else{
        menuIcon.value = "<i class='bx bxs-chevron-left'></i>";
        menuListDisplay.value = "none";
    }
}
</script>

<style scoped>
.ctn {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.desktop-menu {
    color: hsl(0, 0%,100%);
    display: flex;
    flex-direction:row;
    justify-content: space-between;
    gap:0.7vw;
    font-size: 16px;
}
.mobile-menu{
    display:none;
    background-color: hsl(0, 0%, 100%);
    color: hsl(0, 0%, 0%);
    padding:1px 5px;
    width:30px;
}
.menu-icon-ctn{
    color: hsl(0, 0%, 0%);
    font-size:20px;
    margin-right:0;
    display: flex;
    place-items:center;
    justify-content: center;
}
.menu-icon-ctn:hover{
    transition: all .4s;
    cursor: pointer;
    transform: scaleX(1.3);
}
.menu-list-ctn{
    height:200px;
    position: absolute;
    top:60px;
    right:0;
    padding:30px 6px;
    background-color: black;
    color:hsl(0, 0%, 100%);
    flex-direction:column;
    justify-content: space-between;
    gap:0.7vw;
    font-size: 16px;
    border-radius:0 0 0 20px;
}
@media screen and (max-width:850px){
    .desktop-menu{
        display:none;
    }
    .mobile-menu{
        display:flex;
    }
}
</style>

<template>
    <div class="ctn">
        <div class="desktop-menu">
            <IconMenu/>
        </div>
        <div class="mobile-menu">
            <div class="menu-icon-ctn" v-html="menuIcon" @click="showIcons"></div>
            <div class="menu-list-ctn" :style="{ display:menuListDisplay}">
                <IconMenu/>
            </div>
        </div>
    </div>
</template>