<template>
    <div>
        <van-field 
        v-model="content"
        :label="label" 
        :type="type" 
        :placeholder="placeholder"
        :rule="rule"
        />
    </div>
</template>

<script>
export default {
    data(){
        return {
           content:''
        }
    },
    name:"LoginText",
    props:['label','type','placeholder','rule'],
    methods:{
         handlerule() {
            const rue = new RegExp(this.rule)
            //test() 方法用于检测一个字符串是否匹配某个模式.
            if(rue.test(this.content)) {
               this.$emit('inputChange',this.content)         
            }    
         }
    },
    watch:{
        content() {
            this.handlerule()
        }
    }
    
}
</script>

<style scoped>

</style>