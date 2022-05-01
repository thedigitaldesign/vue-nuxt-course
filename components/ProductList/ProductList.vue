<template>
  <div v-for="(info, index) in products" :key="index" class="group relative">
    <ProductListCard :product="info" />
  </div>
</template>

<script lang="ts">
  interface product {
    id: number,
    name: string,
    href: string,
    imageSrc: string,
    imageAlt: string,
    price: number,
    color: string
  }

  const products:product[] = [
    {
      id: 1,
      name: 'Basic Black Tee',
      href: `/products/1`,
      imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-01.jpg',
      imageAlt: "Front of women's Basic Tee in Black.",
      price: 35,
      color: 'Black',
    },
    {
      id: 2,
      name: 'Basic Aspen White Tee',
      href: '#',
      imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-02.jpg',
      imageAlt: "Front of women's Basic Tee in Aspen White.",
      price: 35,
      color: 'Aspen White',
    },
    {
      id: 3,
      name: 'Basic Charcoal Tee',
      href: '#',
      imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-03.jpg',
      imageAlt: "Front of women's Basic Tee in Charcoal.",
      price: 35,
      color: 'Charcoal',
    },
    {
      id: 4,
      name: 'Artwork Tee',
      href: '#',
      imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-04.jpg',
      imageAlt: "Front of women's Artwork Tee.",
      price: 35,
      color: 'Artwork',
    }
  ]

  export default {
    setup() {
      return {
        products
      }
    }
  }
</script>
