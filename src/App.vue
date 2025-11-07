<script setup>
import { ref } from 'vue'
import Promotion_Component from './components/Promotion_Component.vue'
import Category_Component from './components/Category_Component.vue'

const Category_Datas = ref([
  { imgScr: '/img/image1.png', categoryName: 'Cake & Milk', quantity: 14, cardColor: '#F2FCE4' },
  { imgScr: '/img/image2.png', categoryName: 'Peach', quantity: 17, cardColor: '#FFFCEB' },
  { imgScr: '/img/image3.png', categoryName: 'Organic Kiwi', quantity: 21, cardColor: '#ECFFEC' },
  { imgScr: '/img/image4.png', categoryName: 'Red Apple', quantity: 68, cardColor: '#FEEFEA' },
  { imgScr: '/img/image5.png', categoryName: 'Snack', quantity: 34, cardColor: '#FFF3EB' },
  { imgScr: '/img/image6.png', categoryName: 'Black plum', quantity: 25, cardColor: '#FFF3FF' },
  { imgScr: '/img/image7.png', categoryName: 'Vegetables', quantity: 65, cardColor: '#F2FCE4' },
  { imgScr: '/img/image8.png', categoryName: 'Headphone', quantity: 33, cardColor: '#FFFCEB' },
  { imgScr: '/img/image9.png', categoryName: 'Cake & Milk', quantity: 54, cardColor: '#F2FCE4' },
  { imgScr: '/img/image10.png', categoryName: 'Orange', quantity: 63, cardColor: '#FFF3FF' },
])

const Promotion_Datas = ref([
  {
    promotionText: 'Everyday Fresh & Clean with Our Products',
    promotionImg: '/img/image11.png',
    promotionColor: '#F0E8D5',
    btnColor: '#3BB77E',
  },
  {
    promotionText: 'Make your Breakfast Healthy and Easy',
    promotionImg: '/img/image12.png',
    promotionColor: '#F3E8E8',
    btnColor: '#3BB77E',
  },
  {
    promotionText: 'The best Organic Products Online',
    promotionImg: '/img/image13.png',
    promotionColor: '#E7EAF3',
    btnColor: '#FDC040',
  },
])
</script>

<template>
  <div class="Category_Component">
    <Category_Component
      v-for="(cat, index) in Category_Datas"
      :key="index"
      class="box"
      :imgScr="cat.imgScr"
      :categoryName="cat.categoryName"
      :quantity="cat.quantity"
      :cardColor="cat.cardColor"
    />
  </div>

  <div class="Promotion_Component">
    <Promotion_Component
      v-for="(promo, index) in Promotion_Datas"
      :key="index"
      class="box"
      :promotionText="promo.promotionText"
      :promotionImg="promo.promotionImg"
      :promotionColor="promo.promotionColor"
      :btnColor="promo.btnColor"
    />
  </div>
</template>

<style scoped>
.Category_Component,
.Promotion_Component {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  padding: 10px;
}
</style>
