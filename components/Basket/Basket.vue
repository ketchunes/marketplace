<template>
  <dialog id="basket_modal" class="modal">
    <div class="modal-box">
      <form method="dialog">
        <div class="flex items-center justify-between">
          <h3 class="font-medium text-xl h-fit">Корзина</h3>
          <button class="btn btn-square btn-ghost rounded-lg">
            <svg
              class="w-10 h-10"
              viewBox="0 -0.5 25 25"
              fill="none"
              xmlns="http://www.w3.org/2000/svg">
              <path
                class="fill-base-content"
                d="M6.96967 16.4697C6.67678 16.7626 6.67678 17.2374 6.96967 17.5303C7.26256 17.8232 7.73744 17.8232 8.03033 17.5303L6.96967 16.4697ZM13.0303 12.5303C13.3232 12.2374 13.3232 11.7626 13.0303 11.4697C12.7374 11.1768 12.2626 11.1768 11.9697 11.4697L13.0303 12.5303ZM11.9697 11.4697C11.6768 11.7626 11.6768 12.2374 11.9697 12.5303C12.2626 12.8232 12.7374 12.8232 13.0303 12.5303L11.9697 11.4697ZM18.0303 7.53033C18.3232 7.23744 18.3232 6.76256 18.0303 6.46967C17.7374 6.17678 17.2626 6.17678 16.9697 6.46967L18.0303 7.53033ZM13.0303 11.4697C12.7374 11.1768 12.2626 11.1768 11.9697 11.4697C11.6768 11.7626 11.6768 12.2374 11.9697 12.5303L13.0303 11.4697ZM16.9697 17.5303C17.2626 17.8232 17.7374 17.8232 18.0303 17.5303C18.3232 17.2374 18.3232 16.7626 18.0303 16.4697L16.9697 17.5303ZM11.9697 12.5303C12.2626 12.8232 12.7374 12.8232 13.0303 12.5303C13.3232 12.2374 13.3232 11.7626 13.0303 11.4697L11.9697 12.5303ZM8.03033 6.46967C7.73744 6.17678 7.26256 6.17678 6.96967 6.46967C6.67678 6.76256 6.67678 7.23744 6.96967 7.53033L8.03033 6.46967ZM8.03033 17.5303L13.0303 12.5303L11.9697 11.4697L6.96967 16.4697L8.03033 17.5303ZM13.0303 12.5303L18.0303 7.53033L16.9697 6.46967L11.9697 11.4697L13.0303 12.5303ZM11.9697 12.5303L16.9697 17.5303L18.0303 16.4697L13.0303 11.4697L11.9697 12.5303ZM13.0303 11.4697L8.03033 6.46967L6.96967 7.53033L11.9697 12.5303L13.0303 11.4697Z" />
            </svg>
          </button>
        </div>
      </form>

      <form name="basket" method="post" action="./mail/mail.php">
        <div class="divider"></div>
        <span v-if="localItems.length === 0">В корзине пока пусто  : &#41</span>
        <div v-else class="flex flex-col gap-5">
          <BasketItem :item="item" v-for="item in localItems" />
        </div>
        <button @click="localItems = []" class="btn btn-error">Clear</button>
        <div class="divider"></div>

        <!-- if there is a button in form, it will close the modal -->
        <div class="font-medium mb-1.5">Данные</div>
        <div class="grid gap-2 mb-4">
          <input
            type="text"
            placeholder="Ваше имя"
            class="input input-bordered w-full"
            name="name"
            required />
          <input
            type="mail"
            placeholder="Почта"
            class="input input-bordered w-full"
            name="email"
            required />
          <input
            type="text"
            placeholder="Номер телефона"
            class="input input-bordered w-full"
            name="phone"
            required />
        </div>
        <div class="font-medium mb-1.5">Доставка</div>
        <div class="grid gap-1.5 mb-4">
          <input type="text" placeholder="Город" class="input input-bordered w-full" required />
        </div>
        <div class="font-medium mb-2">Способ оплаты</div>
        <div class="grid gap-1.5">
          <div class="flex items-center">
            <input type="radio" name="payment" value="visa" class="radio mr-2.5" required />
            <span>Кредитной картой (Visa, Mastercard)</span>
          </div>
          <div class="flex items-center">
            <input type="radio" name="payment" value="kaspi" class="radio mr-2.5" required />
            <span>Кредитной картой (Kaspi)</span>
          </div>
        </div>
        <div class="text-right font-medium my-6">
          <span>Итоговая сумма:</span>
          <span id="total"> 100000 </span>
          <span>Тг.</span>
        </div>
        <input type="submit" value="Купить" class="btn w-full" />

        <div class="text-center text-sm mt-4">
          Нажимая на кнопку "Купить", вы даете согласие на обработку персональных данных в
          соответствии с
          <span class="underline font-medium">политикой конфиденциальности</span>, а так же с
          <span class="underline font-medium">публичной офертой</span>
        </div>
      </form>
    </div>

    <form method="dialog" class="modal-backdrop">
      <button>close</button>
    </form>
  </dialog>
</template>

<script setup>
  const localItems = useLocalStorage("items", []);
</script>
