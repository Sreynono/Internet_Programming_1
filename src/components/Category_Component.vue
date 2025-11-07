<script setup>
    const props = defineProps({
        imgScr:{
            type: String,
            required: true
        }, 
        categoryName:{
            type: String,
            required: true
        },
        quantity:{
            type: Number,
            required: true
        },
        cardColor:{
            type:String,
            default: 'gray'
        }
    }) 

</script>

<template>
  <div class="categoryCard" :style="{backgroundColor: cardColor}">
        <img class="categoryImg" :src="imgScr" :alt="categoryName">
        <h3 class="categoryName">{{categoryName}}</h3>
        <p class="categoryQuant">{{ quantity }} items</p>
  </div>
</template>

<style scoped>
    .categoryCard{
        width: 136px;
        height: 167px;
        border-radius: 10px;
        display: flex;              /* enable flex layout */
        flex-direction: column;     /* stack items vertically */
        justify-content: center;    /* center vertically */
        align-items: center;        /* center horizontally */
        text-align: center;         /* optional: center text */
    }
    .categoryImg{
        width: 50%;
        height: 50%;
    }
    .categoryName{
        font-size: 14px;
        font-weight: 600;
    }
    .categoryQuant{
        font-size: 12px;
        color: #777;
    }
</style>
