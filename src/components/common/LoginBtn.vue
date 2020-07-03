<template>
    <div class="btnparent" @click="registerClick">
        <div class="loginbtn">{{btntext}}</div>
    </div>
</template>

<script>
export default {
    name:"LoginBtn",
    props:['btntext'],
    methods:{
        registerClick() {
            this.$emit('registerSubmit')
        }
    }
}
</script>

<style scoped>
.btnparent{
    padding: 15px 10px;
}
.loginbtn {
   height: 12.5vw;
   background-color: #ff9bd5;
   color: white;
   display: flex;
   justify-content: center;
   align-items: center;
   border-radius: 6.25vw;
   font-size: 4.444vw;
}
</style>