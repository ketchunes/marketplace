<template>
  <div class="grid gap-5">
    <div class="flex xs:flex-row flex-col gap-5">
      <div class="xs:w-2/3 w-full flex gap-3">
        <img class="w-24 object-cover" :src="item.img" alt="" />
        <div class="flex flex-col gap-2 justify-between">
          <div class="text-sm max-h-14 text-ellipsis overflow-hidden">{{ item.title }}</div>
          <div class="icontent">
            <div class="text-xs mb-2">Размер:</div>
            <select name="size" class="select select-bordered w-full max-w-xs">
              <option value="m">M</option>
              <option value="l">L</option>
              <option value="xl">XL</option>
              <option value="xxl">XXL</option>
            </select>
          </div>
        </div>
      </div>
      <div class="xs:w-1/3 w-full flex xs:flex-col flex-row justify-around">
        <div class="w-full flex gap-2 xs:justify-end justify-center items-center">
          <div @click="quantity > 0 && quantity--" class="w-5 h-5 min-h-5 btn btn-circle btn-outline group">
            <svg width="8" height="2" viewBox="0 0 8 2" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path class="group-hover:invert stroke-base-content" d="M0 1H7.5" />
            </svg>
          </div>
          <div>{{ quantity }}</div>
          <div @click="quantity++" class="w-5 h-5 min-h-5 btn btn-circle btn-outline group">
            <svg width="8" height="8" viewBox="0 0 8 8" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path class="group-hover:invert stroke-base-content" d="M0 4H8" />
              <path class="group-hover:invert stroke-base-content" d="M4 0V8" />
            </svg>
          </div>
        </div>
        <div class="w-full flex xs:justify-end justify-center items-center gap-2">
          <div class="grid gap-1">
            <div class="flex flex-col gap-x-5"></div>
          </div>
          <button @click.prevent="deleteItemById(item.id, localItems)" class="w-5 h-5 min-h-5 btn btn-circle btn-outline group">
            <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path class="group-hover:invert stroke-base-content" d="M3.23389 8.88959L8.76555 3.11026" />
              <path class="group-hover:invert stroke-base-content" d="M3.11005 3.23413L8.88938 8.7658" />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const quantity = ref(0);
  const localItems = useLocalStorage("items", []);

  defineProps({
    item: {
      type: Object,
      required: true,
    },
  });

  function deleteItemById(itemId, itemsArray) {
    const index = itemsArray.findIndex((item) => {
      return item.id === itemId;
    });
    itemsArray.splice(index, 1);
  }
</script>
