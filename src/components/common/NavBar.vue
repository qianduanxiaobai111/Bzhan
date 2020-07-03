<template>
    <div class="navbar">
        <div class="logo">
            <img src="../../assets/img/logo.png" alt="">
        </div>
        <div class="center">
            <p>
                请输入内容
                <van-icon class="input-icon" name="search" />
            </p>
        </div>
        <div class=right>
            <img src="../../assets/img/default_img.jpg" alt="">
            <p>下载App</p>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.navbar {
    height: 12.5vw;
    background-color:white;
    display: flex;
}
.logo {
    width: 30.556vw;
    display: flex;
    justify-content: center;
    align-items: center;
}
.logo img {
    width: 90%;
}
.center {
    flex:1;
    display: flex;
    margin: 0 1.389vw;
    align-items: center;
}
.center p {
    font-size: 3.333vw;
    line-height: 7.222vw;
    height: 7.222vw;
    position: relative;
    background-color:#f4f4f4;
    padding-left: 8.333vw;
    width: 100%;
    border-radius: 3.611vw;
    color: #aaa;
}
.input-icon{
    position: absolute;
    left:2.778vw;
    top:50%;
    transform: translate(0, -50%);
    color: #aaa;

    
}
.right {
    display: flex;
    justify-content: center;
    align-items: center;
}
.right img {
    width: 6.667vw;
    height: 6.667vw;
}
.right p {
    padding:1.389vw 2.778vw;
    margin: 0 2.222vw;
    background-color:#fb7294;
    color: #ffff;
    font-size: 3.611vw;
    border-radius: 1.389vw;
}


</style>