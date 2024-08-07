<script setup>
import navItems from "@/data/nav-items.json";
</script>

<style scoped>
.ctn{
    background-color: transparent;
    color: hsl(0, 0%, 100%);
    display:flex;
    flex-direction:row;
    justify-content:space-between;
    gap:20px;
    text-transform: uppercase;
    font-size:12px;
}
.nav-ctn:hover{
    cursor:pointer;
    transform: scaleX(0.95);
    transition: all .4s;
    color: hsl(160, 17%, 51%);
}
.nav-ctn:active {
    transform: scaleX(0.95);
    transition: all 14s;
    color: hsl(160, 17%, 51%);
}

</style>


<template>
    <div class="ctn">
        <div class="nav-ctn" v-for="navItem in navItems" :key="navItem.id">
            <p class-="nav-p">{{navItem.item}}</p>
        </div>
    </div>
</template>