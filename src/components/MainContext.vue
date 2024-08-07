<style scoped>
.ctn{

}
.ctn p{
    background-color:hsl(0, 0%, 0%);
    color: hsl(0, 0%, 100%);
    padding:10px;
    width:20%;
    border-radius:50%;
    text-transform:uppercase;
    font-size: 10px;
    font-family: "Roboto Condensed", sans-serif;
}
.ctn h1{
    font-family: "Roboto Condensed", sans-serif;
    text-transform: uppercase;
    letter-spacing:-2px;
}
.ctn h1 b{
    font-family: "Major Mono Display", monospace;
    font-size:80px;
    margin-top:-100px;
    letter-spacing: 4px;
}
.btn-ctn{
    font-family: "Roboto Condensed", sans-serif;
    display:flex;
    flex-direction:row;
    gap:1vw;
}
.learn, .shop{
    background-color:hsl(0, 0%, 0%);
    color: white;
    font-size:12px;
    text-transform:uppercase;
    padding: 10px 20px;
}
.learn:hover, .shop:hover{
    cursor:pointer;
    background-color:transparent;
    color:hsl(0, 0%, 0%);
    border: 1px solid hsl(0, 0%, 0%);
    transform: scale(1.1);
    transition: all .4s ease-in-out;
}

</style>

<template>
    <div class="ctn">
        <p>Premium collection</p>
        <h1>the heritage<br/><b>collection</b></h1>
        <br/>
        
        <div class="btn-ctn">
            <button class="learn">
                Learn more
            </button>
            <button class="shop">
                Shop
            </button>
        </div>
    </div>
</template>