<template>
    <div>
    <v-title title="Vue组件化"></v-title>
    <v-button @click="handleClick">点击了按钮</v-button> 
    <!-- 父组件的内容主要基于子组件，一般看父组件看属性和事件就ok了 -->
    <p>
        <img src="./test.jpg" alt="">
    </p>
    </div>

</template>

<script>
    import vTitle from './title.vue'
    import VButton from './button.vue'
    export default {
        components:{
            vTitle,
            VButton
        },
        data(){
            return {
                name:'Vue.js'
            }
        },
        methods:{
            handleClick(e){
                console.log("fatherE"+e);
            }
        }
    }
</script>

<style scoped>
      div{
          color:#f60;
          font-size: 50px;
      }
      img{
        width: 200px;
        height: 200px;
      }
</style>