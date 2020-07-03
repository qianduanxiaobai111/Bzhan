<template>
    <div>
        <nav-bar class="userinfo" />
        <img src="../assets/img/bannerTop_new.png" alt="" class="backimg">
        <user-detail :userInfo="model"/>
        <user-article />

    </div>
</template>

<script>
import NavBar from '../components/common/NavBar'
import userDetail from '../components/usercompnent/userDetail'
import userArticle from '../components/usercompnent/userArtical'


export default {
    data() {
        return {
            model:{}
        }
    },
    components:{
        NavBar,
        userDetail,
        userArticle 
    },
    methods:{
        async UserinfoData() {
            const res = await this.$http.get('/user/' + localStorage.getItem('id'))
            this.model = res.data[0]  
        }
    },
    created() {
        this.UserinfoData()
    }

    
}
</script>

<style scoped>

.backimg{
    height: 100px;
    width: 100%;
}
</style>