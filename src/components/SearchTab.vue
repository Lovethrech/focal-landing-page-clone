<style scoped>
.ctn{
    width: 90%;
    height:100%;
    display:space-between;
}
.input-search{
    background-color: rgba(255, 255, 255, 0.521);
    width:90%;
    height:100%;
    border-radius:20px 0 0 20px;
    border:0;
    padding:0 14px;
}
.input-search::placeholder{
    color: rgb(0, 0, 0);
}
.ctn button{
    height:100%;
    width:10%;
    background-color: hsl(0, 0%, 0%);
    color: hsl(0, 0%, 100%);
    border:0;
    font-size:12px;
    text-transform: uppercase;
    letter-spacing:4px;
}
</style>

<template>
    <div class="ctn">
        <input type="text" placeholder="Search..." class="input-search">
        <button type="button">Search</button>
    </div>
</template>