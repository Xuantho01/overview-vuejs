<template>
    <div class="demo-ref">
        <input type="file"
               ref="fileInPutAvatar"
               style="display: none">
        <h1>Ref demo</h1>
        <button class="avartar"
        v-on:click="handleClickInputFile"> Thay doi Avatar</button>
    </div>
</template>

<script>
    export default {
        name: "Ref",
        methods: {
            handleClickInputFile(){
             }
        }
    }
</script>

<style scoped>
    .demo-ref{
        margin-top: 100px;
        padding: 100px 30px;
        border: 1px solid black;
    }
    .avartar{
        color: #ffffff;
        padding: 12px 15px;
        background-color: #333333;
        transition: all .3s ease;
    }
    .avartar:hover{
        color: #333;
        background-color: #ffffff;
    }
</style>
