<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import SearchTab from "@/components/SearchTab.vue";

const openMailMessage = ref("You have no mail currently.");
const displayMailMessage = ref("none");
const timeout = ref(null);

const openMail = () => {
    if (displayMailMessage.value === "none") {
        displayMailMessage.value = "flex";
    }
    setInterval(() => {
        displayMailMessage.value = "none";
    }, 3000);
}
</script>


<style scoped>
.mail-ctn i:hover{
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
}
</style>

<template>
    <div class="mail-ctn">
        <i class='bx bx-envelope' @click="openMail"></i>
        <div class="mail" :style="{ display: displayMailMessage }">
            <p>{{ openMailMessage }}</p>
        </div>
    </div>
    <div class="search">
        <i class='bx bx-search-alt-2'></i>   
        <div class="search">
            <SearchTab/>
        </div>
    </div>
    
    <i class='bx bx-user'></i>
    <div class="div">
        <div class="shop-bag">
            <i class='bx bxs-shopping-bags'></i>
            <p class="shop-no">0</p>
        </div>
    </div>
</template>