<template>
    <div class="userdetail">
        <div clss="content">
            <div class="user_img">
                <img :src="userInfo.user_img" alt="" v-if="userInfo.user_img">
                <img src="../../assets/img/default_img.jpg" alt v-else />
            </div>
            <div clas="user_edit">
                <div clsss="top_info">
                    <p>
                        <span>0</span><span>粉丝</span>
                    </p>
                    <p>
                        <span>54</span><span>关注</span>
                    </p>
                    <p>
                        <span>0</span><span>获赞</span>
                    </p>
                </div>
                <div @click="$router.push('/edit')">
                    <div class="user_editBtn">编辑资料</div>
                </div>
            </div>
        </div>
        <div>
            <h2>{{userInfo.name}}</h2>
            <p v-if="userInfo.user_desc">{{userInfo.user_desc}}</p>
            <p v-else>这个人很神秘，什么都没有写</p>
        </div>
    </div>
</template>

<script>
export default {
   props:['userInfo']
}
</script>

<style scoped>
.userdetail {
    background-color: #fff;
    padding: 0 12px;
   
    
}
/* .userdetail>div:nth-child(1) {
    display: flex;
    
} */
.userdetail>div:nth-child(1) {
    display: flex;
    
}
.user_img img {
    width: 85px;
    border-radius: 85px;
    margin-right: 20px;
}
/* .user_edit {
    flex:1;
} */
.userdetail div div:nth-child(2) {
    flex:1;
}

.userdetail> div div:nth-child(1)  {  
    display: flex; 
}
.userdetail> div div:nth-child(1) p {
    flex:1;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font-size: 13px;
}
.userdetail> div div:nth-child(1) p:nth-child(1),p:nth-child(2){
    border-right: 1px solid black;
}
.userdetail> div div:nth-child(2) {
    padding: 5px 10px;
}
.userdetail> div div:nth-child(2) .user_editBtn {
    border: 1px solid #fb7a9f;
    justify-content: center;
    padding: 3px;
    align-items: center;
    border-radius: 5px;
    color:pink
}
.userdetail div:nth-child(2) h2 {
    margin: 10px 0 3px 0;
    padding: 0;
    font-weight: 400;
}
.userdetail div:nth-child(2) p {
    border: none;
    padding: 0;
    
}



</style>