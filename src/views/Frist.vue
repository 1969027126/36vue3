<template>
    <div>
        <h1>问卷调查表填写</h1><br>
        <p>1.请问您的性别是：</p>
        <p><input type="radio" name="sex"  value="男" v-model="sex">男
            <input type="radio" name="sex" value="女" v-model="sex">女
            <input type="radio" name="sex" >保密</p>
        <button @click="doSex()">下一页</button>
        <button @click="reSet()">重置</button>
    </div>
</template>

<script>
    import router from "../router";

    export default {
        name: "Frist",
        data(){
            return{
                sex:''
            }
        },
        methods:{
            doSex(){
                this.$router.push('/Second')
                this.$store.commit("doSex",this.sex)
            },
            reSet(){
                  this.sex='none'
            }
        }
    }
</script>

<style scoped>
button{margin-left: 30px;text-decoration: none}
</style>