<template>
  <nuxt-link :to="product.href">
    <div class="w-full min-h-80 bg-gray-200 aspect-w-1 aspect-h-1 rounded-md overflow-hidden group-hover:opacity-75 lg:h-80 lg:aspect-none">
      <img :src="product.imageSrc" :alt="product.imageAlt" class="w-full h-full object-center object-cover lg:w-full lg:h-full" />
    </div>

    <div class="mt-4 flex fustify-between">
      <h3 class="text-sm text-gray-700">{{ product.name }}</h3>
      <p class="mt-1 text-sm text-gray-500">{{ product.color }}</p>
      <p class="text-sm font-medium text-gray-900">{{ product.price }}</p>
    </div>
  </nuxt-link>
</template>

<script lang="ts">
interface products {
  id: number
  name: string
  href: string
  imageSrc: string
  imageAlt: string
  price: number
  color: string
}

export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  }
}
</script>
