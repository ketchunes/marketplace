<template>
  <div class="p-3 2xl:px-32">
    <div class="navbar bg-base-100 justify-between gap-10">
      <div class="navbar-start gap-3">
        <div class="text-xl flex items-center gap-4">
          <div><img src="../public/img/logo.png" alt="" /></div>
          <div>
            <div class="text-md xl:text-3xl">FASHION | DSTYLE</div>
            <div class="text-base lg:text-md">Man, Woman</div>
          </div>
        </div>
      </div>
      <div class="navbar-center hidden lg:flex">
        <a href="#katalog">
          <div class="border-2 border-secondary py-2 px-5 rounded-2xl xl:px-10 hover:bg-secondary group">
            <div class="size-full flex items-center gap-3 hover:border-transparent">
              <div>
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                  <rect class="group-hover:fill-base-100 fill-secondary" width="9" height="9" />
                  <rect class="group-hover:fill-base-100 fill-secondary" x="11" width="9" height="9" />
                  <rect class="group-hover:fill-base-100 fill-secondary" x="11" y="11" width="9" height="9" />
                  <rect class="group-hover:fill-base-100 fill-secondary" y="11" width="9" height="9" />
                </svg>
              </div>
              <div class="text-md group-hover:text-base-100">Каталог одежды</div>
            </div>
          </div>
        </a>
      </div>
      <div class="navbar-end gap-5 hidden md:flex">
        <div class="flex gap-5">
          <div class="flex gap-5">
            <a href="#about" class="hover:cursor-pointer hover:text-secondary">
              <div class="text-xl md:text-base lg:text-lg xl:text-xl flex gap-2">
                <div>О</div>
                <div>нас</div>
              </div>
            </a>
            <a href="#woman" class="hover:cursor-pointer hover:text-secondary">
              <div class="text-xl md:text-base lg:text-lg xl:text-xl">Распродажа</div>
            </a>
          </div>
          <div class="flex gap-5">
            <a href="#category" class="hover:cursor-pointer hover:text-secondary">
              <div class="text-xl md:text-base lg:text-lg xl:text-xl">Популярное</div>
            </a>
            <a href="#footer" class="hover:cursor-pointer hover:text-secondary">
              <div class="text-xl md:text-base lg:text-lg xl:text-xl">Корзина</div>
            </a>
          </div>
        </div>
        <div class="gap-4 hidden 2xl:flex items-center">
          <div>
            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 22 22" fill="none">
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M11 22C4.92487 22 0 17.0751 0 11C0 4.92487 4.92487 0 11 0C17.0751 0 22 4.92487 22 11C22 17.0751 17.0751 22 11 22ZM11.4756 8.25507C10.4905 8.66485 8.52148 9.51297 5.56869 10.7995C5.08921 10.9901 4.83803 11.1767 4.81517 11.3591C4.77652 11.6673 5.16254 11.7887 5.68819 11.954C5.7597 11.9765 5.83378 11.9998 5.90974 12.0245C6.4269 12.1926 7.12258 12.3892 7.48423 12.397C7.81229 12.4041 8.17844 12.2689 8.58267 11.9913C11.3416 10.129 12.7657 9.18768 12.8551 9.16738C12.9182 9.15307 13.0056 9.13507 13.0648 9.18771C13.124 9.24035 13.1182 9.34004 13.112 9.36679C13.0737 9.52981 11.5585 10.9385 10.7743 11.6675C10.5298 11.8948 10.3564 12.056 10.321 12.0928C10.2416 12.1753 10.1607 12.2533 10.0829 12.3283C9.60243 12.7915 9.24213 13.1388 10.1028 13.706C10.5165 13.9786 10.8474 14.204 11.1776 14.4288C11.5382 14.6744 11.8979 14.9193 12.3633 15.2244C12.4818 15.3021 12.5951 15.3828 12.7053 15.4615C13.125 15.7606 13.502 16.0294 13.9678 15.9866C14.2385 15.9617 14.5181 15.7072 14.6601 14.9481C14.9956 13.1543 15.6552 9.26756 15.8076 7.66594C15.821 7.52562 15.8042 7.34604 15.7907 7.2672C15.7772 7.18837 15.749 7.07605 15.6465 6.9929C15.5252 6.89443 15.3378 6.87366 15.254 6.87506C14.8731 6.88185 14.2886 7.08509 11.4756 8.25507Z"
                  fill="#0CBFD8" />
              </svg>
            </a>
          </div>
          <div>
            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 22 22" fill="none">
                <path
                  d="M7.35534 8.84765C7.414 11.7077 8.844 13.4237 11.352 13.4237H11.4987V11.7883C12.419 11.88 13.1157 12.5547 13.3943 13.4237H14.696C14.5625 12.9299 14.3258 12.47 14.0016 12.0743C13.6774 11.6787 13.2729 11.3562 12.815 11.1283C13.2254 10.8784 13.5798 10.5466 13.8561 10.1535C14.1324 9.76051 14.3247 9.3147 14.421 8.84399H13.2403C12.9837 9.75332 12.221 10.5783 11.4987 10.6553V8.84765H10.3143V12.0157C9.581 11.8323 8.657 10.945 8.61667 8.84765H7.35534Z"
                  fill="#0CBFD8" />
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M11 0C17.0751 0 22 4.92487 22 11C22 17.0751 17.0751 22 11 22C4.92487 22 0 17.0751 0 11C0 4.92487 4.92487 0 11 0ZM5.5 10.78C5.5 8.29033 5.5 7.04733 6.27 6.27C7.051 5.5 8.294 5.5 10.78 5.5H11.22C13.7097 5.5 14.9527 5.5 15.73 6.27C16.5 7.051 16.5 8.294 16.5 10.78V11.22C16.5 13.7097 16.5 14.9527 15.73 15.73C14.949 16.5 13.706 16.5 11.22 16.5H10.78C8.29033 16.5 7.04733 16.5 6.27 15.73C5.5 14.949 5.5 13.706 5.5 11.22V10.78Z"
                  fill="#0CBFD8" />
              </svg>
            </a>
          </div>
          <div class="flex items-center">
            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 22 22" fill="none">
                <path
                  d="M17.1111 0C13.2 0 11 3.33375 11 5C11 3.33375 8.8 0 4.88889 0C0.977778 0 0 3.33375 0 5C0 13.75 11 20 11 20C11 20 22 13.75 22 5C22 3.33375 21.0222 0 17.1111 0Z"
                  fill="#FF0000" />
              </svg>
            </a>
          </div>
          <!-- Basket -->
          <div class="cursor-pointer relative" onclick="basket_modal.show()">
            <div class="absolute -top-3 -right-3">
              <div class="size-5 rounded-full bg-secondary grid place-content-center">
                <span class="text-xs text-primary-content">{{ localItems.length }}</span>
              </div>
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" width="22" height="24" viewBox="0 0 22 22" fill="none">
              <circle cx="11" cy="12" r="11" fill="black" />
              <path
                d="M16.968 11.3647C16.9125 11.1267 16.806 10.9036 16.656 10.7107C16.5039 10.5191 16.3113 10.3634 16.092 10.2548C15.9195 10.1694 15.732 10.1185 15.5401 10.1048C15.4423 9.05495 14.9769 8.07335 14.2261 7.33305C13.3712 6.47945 12.2124 6 11.0043 6C9.7961 6 8.63733 6.47945 7.7824 7.33305C7.03158 8.07335 6.56626 9.05495 6.46846 10.1048C6.27647 10.1185 6.08898 10.1694 5.91648 10.2548C5.69621 10.3618 5.50332 10.5178 5.3525 10.7107C5.20105 10.903 5.09445 11.1266 5.04047 11.3654C4.98649 11.6041 4.98651 11.8519 5.04052 12.0906L5.98248 15.9482C6.1446 16.5393 6.49688 17.0605 6.98488 17.4313C7.47287 17.8022 8.06943 18.002 8.68236 18H13.3082C13.9232 18.0006 14.5213 17.7989 15.0103 17.4259C15.4994 17.053 15.8521 16.5295 16.014 15.9362L16.95 12.0906C17.01 11.853 17.016 11.6046 16.968 11.3647ZM9.10834 15.2163C9.10834 15.3356 9.06093 15.45 8.97654 15.5344C8.89216 15.6188 8.7777 15.6662 8.65836 15.6662C8.53902 15.6662 8.42456 15.6188 8.34018 15.5344C8.25579 15.45 8.20838 15.3356 8.20838 15.2163V12.8525C8.20838 12.7332 8.25579 12.6187 8.34018 12.5343C8.42456 12.45 8.53902 12.4025 8.65836 12.4025C8.7777 12.4025 8.89216 12.45 8.97654 12.5343C9.06093 12.6187 9.10834 12.7332 9.10834 12.8525V15.2163ZM11.4542 15.2163C11.4542 15.2754 11.4426 15.3339 11.42 15.3885C11.3974 15.443 11.3642 15.4926 11.3224 15.5344C11.2807 15.5762 11.2311 15.6094 11.1765 15.632C11.1219 15.6546 11.0634 15.6662 11.0043 15.6662C10.9452 15.6662 10.8867 15.6546 10.8321 15.632C10.7775 15.6094 10.7279 15.5762 10.6861 15.5344C10.6443 15.4926 10.6111 15.443 10.5885 15.3885C10.5659 15.3339 10.5543 15.2754 10.5543 15.2163V12.8525C10.5543 12.7332 10.6017 12.6187 10.6861 12.5343C10.7705 12.45 10.8849 12.4025 11.0043 12.4025C11.1236 12.4025 11.2381 12.45 11.3224 12.5343C11.4068 12.6187 11.4542 12.7332 11.4542 12.8525V15.2163ZM13.8001 15.2163C13.8001 15.3356 13.7527 15.45 13.6683 15.5344C13.584 15.6188 13.4695 15.6662 13.3502 15.6662C13.2308 15.6662 13.1164 15.6188 13.032 15.5344C12.9476 15.45 12.9002 15.3356 12.9002 15.2163V12.8525C12.9002 12.7332 12.9476 12.6187 13.032 12.5343C13.1164 12.45 13.2308 12.4025 13.3502 12.4025C13.4695 12.4025 13.584 12.45 13.6683 12.5343C13.7527 12.6187 13.8001 12.7332 13.8001 12.8525V15.2163ZM7.37442 10.0928C7.47309 9.28743 7.84096 8.53904 8.41837 7.96899C9.10533 7.28537 10.0351 6.90159 11.0043 6.90159C11.9734 6.90159 12.9032 7.28537 13.5901 7.96899C14.1676 8.53904 14.5354 9.28743 14.6341 10.0928H7.37442Z"
                fill="white" />
            </svg>
          </div>
        </div>
      </div>
      <div class="dropdown md:hidden dropdown-end">
        <div tabindex="0" role="button" class="btn btn-ghost md:hidden">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" />
          </svg>
        </div>
        <ul tabindex="0" class="menu menu-sm dropdown-content bg-base-100 rounded-box z-1 mt-3 w-52 p-2 shadow">
          <li>
            <a href="#about">
              <div class="text-md">О нас</div>
            </a>
          </li>
          <li>
            <a href="#woman">
              <div class="text-md">Распродажа</div>
            </a>
          </li>
          <li>
            <a href="#category">
              <div class="text-md">Популярное</div>
            </a>
          </li>
          <li>
            <a href="#footer">
              <div class="text-md">Контакты</div>
            </a>
          </li>
        </ul>
      </div>
    </div>

    <Basket />
  </div>
</template>

<script setup>
  const localItems = useLocalStorage("items", []);
</script>
