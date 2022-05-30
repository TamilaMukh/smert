<template>
  <div class="container ml-auto bg-gray-200">
    <div class="w-full items-center flex justify-between">
      <div v-for="tv of tvs" :key="tv.id" class="flex items-center">
        <div class="w-full items-start bg-white rounded-xl p-6 m-2">
          <div class="w-full flex items-center justify-between">
          <!-- <p class="bg-ggreen text-white rounded-full w-1/6 ">{{ tv.hzchtoeto }}</p> -->
          <p class="bg-ggreen text-white rounded-full px-1 text-sm">0-0-36</p>
          <i class="fas fa-heart"></i>
          </div>
          <img class="ml-6" :src="tv.img" alt="">
          <p class="font-semibold text-sm mb-8">{{ tv.title }}</p>
          <div class="w-52 flex items-center justify-between mb-12">
            <p class="text-sm border p-1 rounded-full">43"</p>
            <p class="text-sm border p-1 rounded-full">50"</p>
            <p class="text-sm border p-1 rounded-full">55"</p>
            <p class="text-sm border p-1 rounded-full">65"</p>
            <p class="text-sm border p-1 rounded-full">75"</p>
          </div>
          <p class="font-semibold">{{ tv.discount }} т</p>
          <p class="text-xs mb-4"><s>{{ tv.price }}</s> т <span class="text-bblue font-semibold">Скидка</span></p>
          <div class="flex items-center text-yyellow text-sm">
            <i class="fas fa-star "></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <p class="text-black ml-2">{{ tv.rating }} (1)</p>
          </div>
          <div class="border-b p-2"></div>
          <div class="mt-4 mb-8">
            <div class="flex items-center">
            <img class="mr-4" :src="tv.options[0].logo" alt="">
            <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div>
            <div class="flex items-center my-4">
              <img class="mr-4" :src="tv.options[0].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div><div class="flex items-center">
              <img class="mr-4" :src="tv.options[0].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
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

        <div class="w-full items-start bg-white rounded-xl p-6 m-2">
          <div class="w-full flex items-center justify-between">
          <!-- <p class="bg-ggreen text-white rounded-full w-1/6 ">{{ tv.hzchtoeto }}</p> -->
          <p class="bg-ggreen text-white rounded-full px-1 text-sm">0-0-36</p>
          <i class="fas fa-heart"></i>
          </div>
          <img class="ml-6" :src="tv.img" alt="">
          <p class="font-semibold text-sm mb-8">{{ tv.title }}</p>
          <div class="w-52 flex items-center justify-between mb-12">
            <p class="text-sm border p-1 rounded-full">43"</p>
            <p class="text-sm border p-1 rounded-full">50"</p>
            <p class="text-sm border p-1 rounded-full">55"</p>
            <p class="text-sm border p-1 rounded-full">65"</p>
            <p class="text-sm border p-1 rounded-full">75"</p>
          </div>
          <p class="font-semibold">{{ tv.discount }} т</p>
          <p class="text-xs mb-4"><s>{{ tv.price }}</s> т <span class="text-bblue font-semibold">Скидка</span></p>
          <div class="flex items-center text-yyellow text-sm">
            <i class="fas fa-star "></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <p class="text-black ml-2">{{ tv.rating }} (1)</p>
          </div>
          <div class="border-b p-2"></div>
          <div class="mt-4 mb-8">
            <div class="flex items-center">
            <img class="mr-4" :src="tv.options[0].logo" alt="">
            <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div>
            <div class="flex items-center my-4">
              <img class="mr-4" :src="tv.options[0].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div><div class="flex items-center">
              <img class="mr-4" :src="tv.options[0].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
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

        <div class="w-full items-start bg-white rounded-xl p-6 m-2">
          <div class="w-full flex items-center justify-between">
          <!-- <p class="bg-ggreen text-white rounded-full w-1/6 ">{{ tv.hzchtoeto }}</p> -->
          <p class="bg-ggreen text-white rounded-full px-1 text-sm">0-0-36</p>
          <i class="fas fa-heart"></i>
          </div>
          <img class="ml-6" :src="tv.img" alt="">
          <p class="font-semibold text-sm mb-8">{{ tv.title }}</p>
          <div class="w-52 flex items-center justify-between mb-12">
            <p class="text-sm border p-1 rounded-full">43"</p>
            <p class="text-sm border p-1 rounded-full">50"</p>
            <p class="text-sm border p-1 rounded-full">55"</p>
            <p class="text-sm border p-1 rounded-full">65"</p>
            <p class="text-sm border p-1 rounded-full">75"</p>
          </div>
          <p class="font-semibold">{{ tv.discount }} т</p>
          <p class="text-xs mb-4"><s>{{ tv.price }}</s> т <span class="text-bblue font-semibold">Скидка</span></p>
          <div class="flex items-center text-yyellow text-sm">
            <i class="fas fa-star "></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <p class="text-black ml-2">{{ tv.rating }} (1)</p>
          </div>
          <div class="border-b p-2"></div>
          <div class="mt-4 mb-8">
            <div class="flex items-center">
            <img class="mr-4" :src="tv.options[0].logo" alt="">
            <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div>
            <div class="flex items-center my-4">
              <img class="mr-4" :src="tv.options[0].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
            </div><div class="flex items-center">
              <img class="mr-4" :src="tv.options[0].logo" alt="">
              <p class="text-xs font-semibold">{{ tv.options[0].title }}</p>
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
</template>

<script>
import axios from 'axios'
export default {
  name: "SinglePage",
  data() {
    return {
      tvs: null
    }
  },
  async mounted() {
    this.tvs = (await axios.get("https://6286235096bccbf32d6fe5bf.mockapi.io/tvs")
    ).data;
  }
}
</script>