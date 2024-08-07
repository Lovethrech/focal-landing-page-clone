<style scoped>
.ctn{
    font-family: "Roboto Condensed", sans-serif;
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
.ctn button:hover{
    transition: all .4s ease-in-out;
    cursor:pointer;
    background-color: rgba(0,0,0,0.5);
    transform:scaleX(0.94);
}
@media screen and (max-width:850px){
    .ctn{
        width:80%;
    }
    .input-search{
        width:80%;
    }
    .ctn button{
        width:20%;
        font-size: 1.8vw;
    }
}
</style>

<template>
    <div class="ctn">
        <input type="text" placeholder="Search..." class="input-search">
        <button type="button">Search</button>
    </div>
</template>