<script setup>
    import Button from './Button_Component.vue';

    const props = defineProps({
        promotionText:{
            type: String,
            required: true
        },
        promotionImg:{
            type: String,
            required: true
        },
        promotionColor:{
            type: String,
            default: 'gray'
        },
        btnColor:{
            type: String,
            default: 'green'
        }

    })
</script>

<template>
    
    <div class="promotionBanner" :style="{ backgroundColor: promotionColor }">
        <div class="text-wrapper">
            <h2>{{ promotionText }}</h2>
            <Button :style="{backgroundColor: btnColor}"></Button>
        </div>
        <div class="image-wrapper">
            <img :src="promotionImg" alt="Img">
        </div>
    </div>
  
</template>

<style scoped>
    .promotionBanner {
        width: 400px;
        height: 300px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 30px;
        border-radius: 10px;
        height: 180px;
        overflow: hidden;
        position: relative;
    }

    .text-wrapper {
        max-width: 50%;
        z-index: 10;
    }

    h2 {
        font-size: 24px;
        font-weight: bold;
        line-height: 1.2;
        margin-bottom: 15px;
        color: #333;
    }

    .image-wrapper {
        position: absolute;
        right: 0;
        top: 0;
        height: 80%;
        padding: 20px;
    }

    img {
        height: 100%;
        width: auto;
        border-radius: 0 10px 10px 0;

    }
</style>
