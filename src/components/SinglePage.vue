<template>
  <div class="bg-white">
    <div class="container mx-auto my-20 bg-main rounded-lg p-4">
    <div class="w-full items-center flex">
      <div v-for="tv of tvs" :key="tv.id" class="flex items-center">

        <div class="w-full items-start bg-white rounded-xl p-6 m-2">
          <div class="w-full flex items-center justify-between">
          <!-- <p @click="showRate = 1" class="bg-ggreen text-white rounded-full px-1 text-sm">{{ tv.credit[0] }}</p> -->
          <p class="bg-ggreen text-white rounded-full px-1 text-sm">{{ tv.credit[0] }}</p>
          <div v-if="showLike === 1"><p @click="showLike = 0" class="bg-gray-200 text-xs text-black p-1 rounded-lg border" >Добавить в желаемое</p></div>
          <div @click="showLike = 1"><i class="fas fa-heart hover:cursor-pointer"></i></div>
          </div>
          <img class="ml-6" :src="tv.img" alt="">
          <div class="flex items-center">
          <p v-if="showInch === 1" class="font-semibold text-sm mb-8 mr-2">{{ tv.inches[0] }}</p>
          <p v-if="showInch === 2" class="font-semibold text-sm mb-8 mr-2">{{ tv.inches[1] }}</p>
          <p v-if="showInch === 3" class="font-semibold text-sm mb-8 mr-2">{{ tv.inches[2] }}</p>
          <p v-if="showInch === 4" class="font-semibold text-sm mb-8 mr-2">{{ tv.inches[3] }}</p>
          <p v-if="showInch === 5" class="font-semibold text-sm mb-8 mr-2">{{ tv.inches[4] }}</p>
          <p class="font-semibold text-sm mb-8">{{ tv.title }}</p>
          </div>
          <div class="w-52 flex items-center justify-between mb-12">
            <p @click="showInch = 1" class="text-sm border p-1 rounded-full hover:cursor-pointer">{{ tv.inches[0] }}</p>
            <p @click="showInch = 2" class="text-sm border p-1 rounded-full hover:cursor-pointer">{{ tv.inches[1] }}</p>
            <p @click="showInch = 3" class="text-sm border p-1 rounded-full hover:cursor-pointer">{{ tv.inches[2] }}</p>
            <p @click="showInch = 4" class="text-sm border p-1 rounded-full hover:cursor-pointer">{{ tv.inches[3] }}</p>
            <p @click="showInch = 5" class="text-sm border p-1 rounded-full hover:cursor-pointer">{{ tv.inches[4] }}</p>
          </div>
          <p class="font-semibold">{{ tv.discount }} т</p>
          <p class="text-xs mb-4"><s>{{ tv.price }}</s> т <span class="text-bblue font-semibold">  Скидка {{ Math.round(tv.price-tv.discount) }} т </span></p>
          <div class="flex items-center text-yyellow text-sm">
            <i class="fas fa-star "></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <p class="text-black ml-2">{{ tv.rating[0].overall }} ({{ tv.rating[0].reviews }})</p>
          </div>
          <div class="border-b p-2"></div>
          <div class="mt-4 mb-8">
            <div class="flex items-center">
            <img class="mr-4 w-6 h-6" :src="tv.options[0].logo" alt="">
            <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div>
            <div class="flex items-center my-4">
              <img class="mr-4 w-6 h-6" :src="tv.options[1].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[1].title }}</p>
            </div><div class="flex items-center">
              <img class="mr-4 w-6 h-6" :src="tv.options[2].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[2].title }}</p>
            </div>
          </div>
          <div class="border-b p-2 mb-2"></div>
          <div>
            <button class="w-full p-1 bg-black text-white rounded-full text-sm mb-2">Добавить в корзину</button><br>
            <button class="w-full p-1 border rounded-full text-sm mb-2">Узнать больше</button>
            <div class="w-full ml-6 my-2 flex items-center"><p class="mr-4 text-xs"><i class="fas fa-map-marker-alt text-xs"></i> Где купить</p> 
            <p class="text-xs"><i class="fas fa-balance-scale-left text-xs"></i> Сравнить</p></div>
          </div>
        </div>

      </div>
    </div>
  </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: "SinglePage",
  data() {
    return {
      tvs: null,
      showLike: 0,
      showInch: 0,
      showRate: 0
    }
  },
  async mounted() {
    this.tvs = (await axios.get("https://6286235096bccbf32d6fe5bf.mockapi.io/tvs")
    ).data;
  }
}
</script>