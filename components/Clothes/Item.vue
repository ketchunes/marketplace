<template>
  <div class="h-full flex flex-col gap-2">
    <div><img class="w-full" :src="item.img" alt="" /></div>
    <div class="text-lg">{{ item.title }}</div>
    <div>{{ item.subTitle }}</div>
    <div class="text-secondary-content mb-auto">{{ item.price }}</div>
    <button
      @click="getIdCallback(item.id)"
      class="active:scale-95 rounded-md hover:cursor-pointer w-fit transition">
      <CardHover
        border-radius="var(--radius-box)"
        container-color="var(--color-base-200)"
        light-color="var(--color-secondary-content)"
        base-color="var(--color-base-200)">
        <div class="py-2 px-4 font-semibold text-sm">ДОБАВИТЬ В КОРЗИНУ</div>
      </CardHover>
    </button>
  </div>
</template>

<script setup>
  defineProps({
    item: {
      type: Object,
      required: true,
    },
    getIdCallback: {
      type: Function,
      required: false,
    },
  });
</script>
