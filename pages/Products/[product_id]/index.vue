<script setup>
definePageMeta({
  middleware: [
    async function (to, from) {
      console.log(`to: `, to)
      console.log(`from: `, from)

      if(!/^\d+$/.test(to.params.product_id)) {
        return abortNavigation(`Page not found!`)
      }
    }
  ]
})
</script>

<template>
  <div>Product Page: {{ $route.params.product_id }}</div>
</template>

<script>
export default {

}
</script>
