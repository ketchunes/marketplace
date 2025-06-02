<template>
  <div class="px-10 py-5 md:px-32">
    <div v-for="category in categories" :key="category.name">
      <div class="text-3xl mt-4 mb-12">{{ category.title }}</div>
      <div class="grid md:grid-cols-2 xl:grid-cols-4 gap-10 mt-3">
        <div v-for="item in getItemsByCategory(category.name, items)" :key="item.img">
          <ClothesItem :item="item" :get-id-callback="(id) => addItem(id, items)" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const categories = [
    {
      name: "woman",
      title: "Женщинам",
    },
    {
      name: "man",
      title: "Мужчинам",
    },
    {
      name: "sale",
      title: "Распродажа",
    },
  ];

  const items = [
    {
      id: 1,
      category: "woman",
      img: "img/cl-2.png",
      title: "ПАРКА ЗИМНЯЯ ЖЕНСКАЯ «МАРИИНКА»",
      subTitle: "Коллекция 2023-2024",
      price: "35.000 Тг.",
    },
    {
      id: 2,
      category: "woman",
      img: "img/cl-1.png",
      title: "ПАРКА ЗИМНЯЯ ЖЕНСКАЯ «МАРИИНКА» ФУКСИЯ",
      subTitle: "Коллекция 2023-2024",
      price: "30.000 Тг.",
    },
    {
      id: 3,
      category: "woman",
      img: "img/cl-3.png",
      title: "ПАРКА ЗИМНЯЯ ЖЕНСКАЯ «МАРИИНКА» ПЕРЛАМУТР",
      subTitle: "Коллекция 2023-2024",
      price: "38.000 Тг.",
    },
    {
      id: 4,
      category: "woman",
      img: "img/cl-4.png",
      title: "КУРТКА КОРОТКАЯ ЗИМНЯЯ ЖЕНСКАЯ «ФОНТАНКА» БЕЖЕВАЯ",
      subTitle: "Коллекция 2023-2024",
      price: "35.000 Тг.",
    },
    {
      id: 5,
      category: "man",
      img: "img/man-1.png",
      title: "ПАРКА ЗИМНЯЯ МУЖСКАЯ «АДМИРАЛТЕЙСТВО» ЧЁРНАЯ",
      subTitle: "Коллекция 2023-2024",
      price: "31.000 Тг.",
    },
    {
      id: 6,
      category: "man",
      img: "img/man-2.png",
      title: "КУРТКА КОРОТКАЯ МУЖСКАЯ «ВЕРФЬ» БЕЖЕВАЯ",
      subTitle: "Коллекция 2023-2024",
      price: "26.400 Тг.",
    },
    {
      id: 7,
      category: "man",
      img: "img/man-3.png",
      title: "ВЕТРОВКА МУЖСКАЯ ЧЁРНАЯ",
      subTitle: "Коллекция 2023-2024",
      price: "12.000 Тг.",
    },
    {
      id: 8,
      category: "man",
      img: "img/man-4.png",
      title: "ПЛАЩ МУЖСКОЙ DEEP BLUE",
      subTitle: "Коллекция 2023-2024",
      price: "17.500 Тг.",
    },
    {
      id: 9,
      category: "sale",
      img: "img/woman-1.png",
      title: "ПАЛЬТО ТЁПЛОЕ ЖЕНСКОЕ «ЭРМИТАЖ» МЯТНОЕ",
      subTitle: "Коллекция 2023-2024",
      price: "17.500 Тг.",
    },
    {
      id: 10,
      category: "sale",
      img: "img/woman-2.png",
      title: "ПАЛЬТО ТЁПЛОЕ ЖЕНСКОЕ «ЭРМИТАЖ» ОРХИДЕЯ",
      subTitle: "Коллекция 2023-2024",
      price: "14.000 Тг.",
    },
    {
      id: 11,
      category: "sale",
      img: "img/woman-3.png",
      title: "ПАЛЬТО ТЁПЛОЕ ЖЕНСКОЕ «ЭРМИТАЖ» ЧЁРНОЕ",
      subTitle: "Коллекция 2023-2024",
      price: "19.600 Тг.",
    },
    {
      id: 12,
      category: "sale",
      img: "img/woman-4.png",
      title: "ПАЛЬТО ТЁПЛОЕ ЖЕНСКОЕ ПЫЛЬНО-ГОЛУБОЕ",
      subTitle: "Коллекция 2023-2024",
      price: "15.400 Тг.",
    },
  ];

  const localItems = useLocalStorage("items", []);

  function addItem(searchedItemId, itemsArray) {
    const item = itemsArray.find((item) => {
      return item.id === searchedItemId;
    });

    if (typeof item !== "undefined") {
      localItems.value.push(item);
    } else {
      throw new Error("Товар не найден");
    }
  }

  function getItemsByCategory(searchedCategory, itemsArray) {
    const items = [];

    itemsArray.find((item) => {
      if (item.category === searchedCategory) {
        items.push(item);
      }
    });

    return items;
  }
</script>
