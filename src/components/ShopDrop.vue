<script setup>
import { ref } from "vue";
import shopDrops from "@/data/shop-drops.json";

const shiftShopPositionStyle = ref({
    position: "absolute",
    top: '20px'
})
const shiftShopPosition = () => {
    shiftShopPositionStyle.value = ({
        position: "relative",
        top: "8px"
    })
}
</script>

<style scoped>
.shop-ctn{
    color: hsl(0, 0%, 100%);
    margin: auto 0;
    display: flex;
    flex-direction: row;
    gap:0.5vw;
}
.shop-ctn:hover, select:hover{
    cursor:pointer;
}
.shop-ctn p{
    text-transform: uppercase;
    letter-spacing: 6px;
}
.shop-ctn p sub{
    font-size: 1px;
}
select{
    background-color:rgba(0, 0, 0, 0);
    color:hsl(0, 0%, 100%);
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
        <p :style="{ position:shiftShopPositionStyle.position, top:shiftShopPositionStyle.top }"><sub>tm</sub>shop</p>
        <select @click="shiftShopPosition">
            <option 
                v-for="shopDrop in shopDrops"  
                :key="shopDrop.id" 
                :value="shopDrop.id"
                >
                    {{ shopDrop.name }}
            </option>
        </select>
    </div>
</template>