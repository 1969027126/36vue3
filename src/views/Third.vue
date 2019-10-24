<template>
    <div>
        <h1>问卷调查表填写</h1>
        <p>3.请介绍一下自己</p>
        <p>{{this.$store.state.checked}}</p>
        <textarea v-model="txt"></textarea><br>
        <button @click="doClick()">提交</button>
        <button><router-link to="/Second">上一页</router-link></button>
        <button>重置</button>
    </div>
</template>

<script>
    export default {
        name: "Third",
        data(){
            return{
                txt: ''
            }
        },
        methods:{
            doClick(){
                this.$router.push('/Four')
                this.$store.commit("doClick",this.txt)
            }
        }
    }
</script>

<style scoped>
button{text-decoration: none;margin-left: 20px;margin-top: 20px}
</style>