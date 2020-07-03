<template>
    <div>
        <login-top middleTop="注册bilibili">
            <div slot="left" @click="$router.go(-1)">
                <img src="../assets/img/fanhui.png" alt="">
            </div>
            
        </login-top>


        <login-text label="姓名" 
        style="margin:4.167vw 0"
        rule="^.{6,16}$"
        placeholder="请输入姓名"
        @inputChange="res => model.name = res"
        /> 
        <login-text label="账号"
        placeholder="请输入账号"
        rule="^.{6,16}$"
        @inputChange="res => model.username = res"
        />
        <login-text label="密码"
        placeholder="请输入密码"
        type="password"
        rule="^.{6,16}$"
        @inputChange="res => model.password = res"
        />
        <login-btn btntext="注册" @registerSubmit="registerSubmit"/>
    </div>
</template>

<script>
import LoginTop from '../components/common/LoginTop'
import LoginText from '../components/common/LoginText'
import LoginBtn from '../components/common/LoginBtn'
export default {
    name:"register",
    data(){
        return {
            model:{
                name:'',
                username:'',
                password:''
            }
        }
    },
   
    components:{
        LoginTop,
        LoginText,
        LoginBtn
    },
    methods:{
        async registerSubmit() {
            let rulg = /^.{6,16}$/
            if(rulg.test(this.model.name) && rulg.test(this.model.username) && rulg.test(this.model.password)) {
                const res = await this.$http.post('/register', this.model)
                this.$msg.success(res.data.msg)  
                console.log(res);  
                localStorage.setItem('token',res.data.objtoken) 
                localStorage.setItem('id',res.data.id)
                if(res.data.msg=='注册成功'){
                    setTimeout(()=>{
                   this.$router.push('/login')
                },1000)}              
            }else {
                this.$msg.fail('格式不正确，清重新输入')    
            }
        }
    }
    
}
</script>

<style scoped>

</style>