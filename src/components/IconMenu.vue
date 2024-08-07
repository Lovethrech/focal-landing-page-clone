<style scoped>
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
        top: 21vh;
        right: 0.2vw;
    }
}
</style>

<template>
    <i class='bx bx-envelope'></i>
    <i class='bx bx-search-alt-2'></i>
    <i class='bx bx-user'></i>
    <div class="div">
        <div class="shop-bag">
            <i class='bx bxs-shopping-bags'></i>
            <p class="shop-no">0</p>
        </div>
    </div>
</template>