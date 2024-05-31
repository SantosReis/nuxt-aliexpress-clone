<template>
  <MainLayout>
    <div id="IndexPage" class="mt-4 max-w-[1200px] mx-auto px-2">
      <div
        class="grid xl:grid-cols-6 lg:grid-cols-5 md:grid-cols-4 sm:grid-cols-3 grid-cols-2 gap-4"
      >
        <div v-if="products" v-for="product in products" :key="product">
          <ProductComponent :product="product" />
        </div>
      </div>
    </div>
  </MainLayout>
</template>

<script setup>
import MainLayout from '~/layouts/MainLayout.vue'

const products = [
  {
    id: 1,
    title: 'Title 1',
    description: 'This is a description',
    url: 'https://picsum.photos/id/7/800/800',
    price: 9899
  },
  {
    id: 2,
    title: 'Title 1',
    description: 'This is a description',
    url: 'https://picsum.photos/id/71/800/800',
    price: 9699
  },
  {
    id: 3,
    title: 'Title 1',
    description: 'This is a description',
    url: 'https://picsum.photos/id/72/800/800',
    price: 29999
  },
  {
    id: 4,
    title: 'Title 1',
    description: 'This is a description',
    url: 'https://picsum.photos/id/73/800/800',
    price: 9699
  },
  {
    id: 5,
    title: 'Title 1',
    description: 'This is a description',
    url: 'https://picsum.photos/id/74/800/800',
    price: 94999
  }
]
// import { useUserStore } from '~/stores/user'
// const userStore = useUserStore()

// let products = ref(null)
// onBeforeMount(async () => {
//   products.value = await useFetch('/api/prisma/get-all-products')
//   setTimeout(() => (userStore.isLoading = false), 1000)
// })
</script>
