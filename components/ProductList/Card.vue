<template>
  <div class="w-full min-h-80 bg-gray-200 aspect-w-1 aspect-h-1 rounded-md overflow-hidden group-hover:opacity-75 lg:h-80 lg:aspect-none">
    <img :src="product.imageSrc" :alt="product.imageAlt" class="w-full h-full object-center object-cover lg:w-full lg:h-full" />
  </div>

  <div class="mt-4 flex justify-between">
    <div>
      <h3 class="text-sm text-gray-700">
        <nuxt-link :to="product.href">
          <span aria-hidden="true" class="absolute inset-0" />
          {{ product.name }}
        </nuxt-link>
      </h3>
      <p class="mt-1 text-sm text-gray-500">{{ product.color }}</p>
    </div>
    <p class="text-sm font-medium text-gray-900">${{ product.price }}</p>
  </div>
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
