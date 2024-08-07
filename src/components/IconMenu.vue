<script setup>
import { ref } from "vue";
import SearchTab from "@/components/SearchTab.vue";

const searchIcon = ref("<i class='bx bx-search-alt-2'></i>");
const showSearch = ref("none");
const openMailMessage = ref("You have no mail currently.");
const displayMailMessage = ref("none");
const openMail = () => {
    if (displayMailMessage.value === "none") {
        displayMailMessage.value = "flex";
    }
    setInterval(() => {
        displayMailMessage.value = "none";
    }, 3000);
}
const search = () => {
    if (searchIcon.value == "<i class='bx bx-search-alt-2'></i>") {
        searchIcon.value = "<i class='bx bx-search-alt'></i>";
        showSearch.value = "flex";
    }
    else{
        searchIcon.value = "<i class='bx bx-search-alt-2'></i>";
        showSearch.value = "none";
    }
}
</script>


<style scoped>
.mail-ctn i:hover, .search-icon:hover{
    cursor: pointer;
}
.mail{
    position:absolute;
    top:6vh;
    right:1vw;
    background-color:hsl(0, 0%, 100%);
    color: hsla(0, 10%, 20%, 0.815);
    padding:4px 6px;
    border-radius: 10px 0 0 10px;
}
.main-search{
    position: absolute;
    top:100px;
    left:0;
    right:0;
    width:100%;
    height:40px;
    display: flex;
    place-items: center;
    justify-content: center;
}
.shop-bag {
    display: flex;
}

.shop-no {
    position: fixed;
    top: 1.3vh;
    right: 4.7vw;
    background-color: hsl(0, 0%, 100%);
    color: hsl(0, 0%, 0%);
    padding: 2px 4px;
    border-radius: 50%;
    font-size: 10px;
}

@media screen and (max-width:850px) {
    .shop-no {
        position: fixed;
        top: 210px;
        right: 0.2vw;
    }
    .mail{
        top:3vh;
        right:6vw;
    }
}
</style>

<template>
    <div class="mail-ctn">
        <i class='bx bx-envelope' @click="openMail"></i>
        <div class="mail" :style="{ display: displayMailMessage }">
            <p>{{ openMailMessage }}</p>
        </div>
    </div>
    <br/>
    <div class="search">
        <div class="search-icon" v-html="searchIcon" @click="search"></div>
        <div class="main-search" :style="{ display: showSearch }">
            <SearchTab/>
        </div>
    </div>
    <br/>
    <div class="user">
        <i class='bx bx-user'></i>   
    </div>
    
    <br/>
    <div class="div">
        <div class="shop-bag">
            <i class='bx bxs-shopping-bags'></i>
            <p class="shop-no">0</p>
        </div>
    </div>
</template>