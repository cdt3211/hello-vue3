<template>
    <div class="person">
        <h2>姓名：{{ name }}</h2>
        <h2>年龄：{{ age }}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="changeAge">修改年龄</button>
        <button @click="showTel">查看联系方式</button>
    </div>
</template>

<!-- <script lang="ts">
    export default{
        name: 'Person234',
    }
</script> -->
<script setup lang="ts" name="Person">
    import {ref} from 'vue'
    //数据
    let name = ref('张三')
    let age = ref(18)
    let tel = '15690024456'

    //方法
    function changeName(){
        name.value = '李四'
    }
    function changeAge(){
        age.value += 1
    }
    function showTel(){
        alert(tel)
    }
</script>

<style>
    .person{
        text-align: center;
    }
</style>