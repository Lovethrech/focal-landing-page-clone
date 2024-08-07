<style scoped>
.ctn{
    background-color: rgba(255, 255, 255, 0.158);
    padding:20px;
    box-shadow: 0px 0px 8px 2px #44444475;
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
    font-size:38px;
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
    box-shadow: 0px 0px 8px 2px #4444448f;
}
.learn:hover, .shop:hover{
    cursor:pointer;
    background-color:transparent;
    color:hsl(0, 0%, 0%);
    border: 1px solid hsl(0, 0%, 0%);
    transform: scale(1.1);
    transition: all .4s ease-in-out;
}

@media screen and (max-width:850px) and (min-width:551px){
    .ctn p {
        font-size:6px;
        min-width: 12%;
        display:flex;
        justify-content: center;
        place-items: center;
    }
    .ctn h1{
        font-size:20px;
    }
    .ctn h1 b{
        font-size:60px;
    }
    .learn, .shop{
        font-size:8px;
    }
}
@media screen and (max-width:550px) {
    .ctn {
        text-align:center;
    }
    .ctn p {
        margin:0 auto;
        width:24%;
        font-size:1.2vw;
    }

    .ctn h1 {
        font-size: 5vw;
    }

    .ctn h1 b {
        font-size: 12vw;
    }
    .btn-ctn{
        place-items: center;
        justify-content: center;
        gap:2vw;
    }
    .learn,
    .shop {
        font-size: 1.5vw;
    }
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