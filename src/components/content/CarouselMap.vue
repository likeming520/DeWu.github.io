<template>
        <div class="map-size">
            <el-carousel :interval="4000" type="card" height="200px">
                <el-carousel-item v-for="(img,index) in imgList" :key="index">
                    <img :src="img.url" width="100%" height="100%">
                </el-carousel-item>
            </el-carousel>
        </div>
</template>

<script>
    export default {
        name: "CarouselMap",
        data() {
            return {
                imgList: [
                    {url:require("@a/img/lunbotu/1.jpg")},
                    {url:require("@a/img/lunbotu/2.jpg")},
                    {url:require("@a/img/lunbotu/3.jpg")},
                    {url:require("@a/img/lunbotu/4.jpg")},
                    {url:require("@a/img/lunbotu/5.jpg")},
                    ]
            }
        }
    }
</script>

<style scoped>
    .el-carousel__item h3 {
        color: #475669;
        font-size: 14px;
        opacity: 0.75;
        line-height: 200px;
        margin: 0;
    }

    .el-carousel__item:nth-child(2n) {
        background-color: #99a9bf;
    }

    .el-carousel__item:nth-child(2n+1) {
        background-color: #d3dce6;
    }

    .map-size {
        width: 600px;
        margin: auto;
        position: relative;
        top: 500px;
    }
</style>