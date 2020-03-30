<template>
    <div class="title text-center">
        <div class="cn">{{cnTitle}}</div>
        <div class="en">{{enTitle}}</div>
    </div>
</template>
<script>
    export default {
        props:['cnTitle','enTitle']
    }
</script>
<style lang="scss">
    .title{
        margin-top: 35px;
        margin-bottom: 35px;
        .cn{
            font-size: 20px;
            line-height: 20px;
            color: #030303;
        }
        .en{
            font-size: 16px;
            line-height: 16px;
            color: #030303;
            margin-top: 10px;
            position: relative;
            &::after{
                margin-top: 8px;
                content: '';
                position: absolute;
                width: 30px;
                height: 2px;
                border-radius: 1px;
                left: 35%;
                top: 0 ;
                background-color: #ff5f35;
            }
            &::before{
                margin-top: 8px;
                content: '';
                position: absolute;
                width: 30px;
                height: 2px;
                border-radius: 1px;
                right: 35%;
                top: 0 ;
                background-color: #ff5f35;
            }
        }
    }
</style>