<template>
    <div class="content">
        <div class="info">
        <h2> SHOPPING<br><span>WASUPPPP</span></h2>
        <p> TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT  </p>
        <a href="#" class="info-btn"> See more</a>
        </div>
    </div>
</template>
<script setup>

</script>
<style>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;

}
.content{
    position: fixed;
    width: 100%;
    min-height: 100vh;
    display:flex;
    flex-direction: column;
    justify-content: flex-start;
    background-color: #968787;
    background-size:contain;
    
}
.info{
    max-width:500px;
    margin: 200px 200px;
}
.content .info h2{
    color: black;
    font-size: 55px;
    text-transform: uppercase;
    font-weight: 800;
    letter-spacing: 2px;
    line-height: 60px;
    margin-bottom: 30px;
}
.content .info p{
    font-size:16px;
    font-weight: 500;
    margin-bottom: 40px;
}
.content .info-btn{
    color: white;
    background: #226a80;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: 2px;
    padding: 10px 20px;
    border-radius: 5px;
    transition: 0.3s;
    transition-property: background;
}
.content .info-btn:hover{
    background: blue;
}
.artwork{
    float: left;
    max-width: 300px;
   
}
</style>











<!-- <div class="banner">
        <div class="container">
            <div class="banner-content">
                <div class="main-banner">
                    <div class="img-container">
                        <img src="@/assets/images/1.avif" alt="">
                        <div class="img-content">
                            <h3>SHOP NOW</h3>
                        </div>
                    </div>
                </div>
                <div class="category-banner">
                    <div class="top">
                        <div class="img-container">
                        <img src="@/assets/images/2.webp" alt="">
                        <div class="img-content">
                            <h3>SHOP NOW</h3>
                        </div>
                    </div>
                    </div>
                </div>
            </div>
        </div>
    </div>-->

    <!--img{
    height: 100%;
}
.banner .container{
    max-width: calc(1440px-170px);
    width: 100%;
    margin: auto;
}
.banner-content{
    display: flex;
    justify-content: space-between;
    height: calc(100vh - 92px);
}
.img-container{
    position: relative;
    height: 100%;
}
.img-container .img-content{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,50%);
    background: white;
    border-radius: 4px;
    padding: 16px 32px;
    text-align: center;-->