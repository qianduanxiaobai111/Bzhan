<template>
    <div>
        <div class="LoginTop">
           <div class="left">
               <slot name="left" />
           </div>
           <div class="center">{{middleTop}}</div>
           <div class="right">
                <slot name="right" />
           </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['middleTop']
}
</script>

<style scoped>
.LoginTop {
    height: 12.222vw;
    background-color:white;
    display: flex;
}
.left {
    flex:1;
    box-sizing: border-box;
    margin-top: 1.389vw;
}
.left img {
    width: 10.556vw;


}
.center {
    display: flex;
    flex:1;
    justify-content: center;
    align-items: center;
    font-size: 4.444vw; 
}
.right {
    flex:1;
    justify-content: center;
    align-items: center;
    font-size: 3.611vw; 
    line-height: 12.222vw;
    text-align: center;
    
}
</style>