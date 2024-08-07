<script setup>
import shopDrops from "@/data/shop-drops.json";
</script>

<style scoped>
.shop-ctn{
    color: hsl(0, 0%, 100%);
    margin: auto 0;
    display: flex;
    flex-direction: row;
    gap:0.5vw;
}
.shop-ctn p{
    position:fixed;
    top:2vh;
    left:48vw;
    margin:auto 0;
    margin-right:-6.6vw;
}
select{
    background-color:rgba(0, 0, 0, 0);
    border-radius:0;
    border: 2px solid hsl(0, 0%, 100%);
    padding:6px 0;
}
option{
    background-color: hsl(0, 0%, 0%);
    color: hsl(0, 0%, 100%);
    text-transform: capitalize;
    margin:20px 0 ;
}
</style>

<template>
    <div class="shop-ctn">
        <p>Shop</p>
        <select>
            <option 
                v-for="shopDrop in shopDrops"  
                :key="shopDrop.id" 
                :value="shopDrop.id">
                    {{ shopDrop.name }}
            </option>
        </select>
    </div>
</template>