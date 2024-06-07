<template>
  <button
    data-drawer-target="default-sidebar"
    data-drawer-toggle="default-sidebar"
    aria-controls="default-sidebar"
    type="button"
    class="inline-flex items-center p-2 mt-2 ms-3 text-sm text-gray-500 rounded-lg sm:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
  >
    <span class="sr-only">Open sidebar</span>
    <svg
      class="w-6 h-6"
      aria-hidden="true"
      fill="currentColor"
      viewBox="0 0 20 20"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        clip-rule="evenodd"
        fill-rule="evenodd"
        d="M2 4.75A.75.75 0 012.75 4h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 4.75zm0 10.5a.75.75 0 01.75-.75h7.5a.75.75 0 010 1.5h-7.5a.75.75 0 01-.75-.75zM2 10a.75.75 0 01.75-.75h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 10z"
      ></path>
    </svg>
  </button>

  <aside
    id="default-sidebar"
    class="fixed top-0 left-0 z-40 w-[90px] h-screen transition-transform -translate-x-full sm:translate-x-0"
    aria-label="Sidebar"
  >
    <div class="h-full px-3 py-4 overflow-y-auto bg-gray-50 dark:bg-gray-800">
      <ul class="space-y-2 font-medium">
        <li>
          <a
            href="#"
            class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
          >
            <svg
              width="40"
              height="40"
              viewBox="0 0 40 40"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M37.3499 29.9385C39.0337 27.0103 40 23.6167 40 19.997C40 8.95315 31.0465 1.10789e-07 20 1.10789e-07C8.95458 -0.00114996 0 8.95184 0 19.9957C0 25.7792 2.45452 30.9889 6.38623 34.642C6.48892 28.9439 6.6683 22.5702 6.97388 20.1974C7.5504 15.7338 11.7394 14.0154 17.2622 9.34154C18.8939 7.95604 21.4487 7.60214 24.7729 9.95519C28.3014 12.4541 31.7975 13.9016 32.9185 15.0448C34.3869 16.5428 33.7164 17.8987 32.3259 17.8987C30.9451 17.8987 28.2778 16.0665 26.453 15.1956C20.506 12.3404 19.9987 12.1177 17.2225 15.2501C14.2744 18.5793 12.5238 21.7945 16.3862 23.7528C19.6957 25.4291 23.0793 21.8637 25.1788 19.3598C27.0295 17.1565 29.4569 17.2889 30.2993 18.3491C31.1418 19.418 29.2713 20.0798 27.9388 21.4382C25.3123 24.1165 26.103 24.7919 24.0529 28.2993C22.3754 31.1706 20.0717 30.9777 17.9413 33.1043C17.1285 33.9109 16.9554 36.849 17.0036 39.7736C17.981 39.9257 18.9818 40 19.9987 40C23.6311 40 27.0344 39.0226 29.974 37.3304L36.771 38.4944C36.771 38.4944 38.8804 38.7356 38.362 35.9583C38.1307 34.7089 37.6877 32.0169 37.3499 29.9385ZM29.8403 11.5771L24.0542 8.40637C25.2541 8.5337 25.7232 8.52877 26.5953 8.68091C27.3351 8.81087 29.729 8.88759 30.3055 9.91444C30.8796 10.9326 29.8403 11.5771 29.8403 11.5771Z"
                fill="#F26522"
              />
            </svg>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex flex-col items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
          >
            <svg
              width="40"
              height="40"
              viewBox="0 0 40 40"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M19.25 13.25V17.75C19.25 18.1478 19.092 18.5294 18.8107 18.8107C18.5294 19.092 18.1478 19.25 17.75 19.25H13.25C12.8522 19.25 12.4706 19.092 12.1893 18.8107C11.908 18.5294 11.75 18.1478 11.75 17.75V13.25C11.75 12.8522 11.908 12.4706 12.1893 12.1893C12.4706 11.908 12.8522 11.75 13.25 11.75H17.75C18.1478 11.75 18.5294 11.908 18.8107 12.1893C19.092 12.4706 19.25 12.8522 19.25 13.25ZM26.75 11.75H22.25C21.8522 11.75 21.4706 11.908 21.1893 12.1893C20.908 12.4706 20.75 12.8522 20.75 13.25V17.75C20.75 18.1478 20.908 18.5294 21.1893 18.8107C21.4706 19.092 21.8522 19.25 22.25 19.25H26.75C27.1478 19.25 27.5294 19.092 27.8107 18.8107C28.092 18.5294 28.25 18.1478 28.25 17.75V13.25C28.25 12.8522 28.092 12.4706 27.8107 12.1893C27.5294 11.908 27.1478 11.75 26.75 11.75ZM17.75 20.75H13.25C12.8522 20.75 12.4706 20.908 12.1893 21.1893C11.908 21.4706 11.75 21.8522 11.75 22.25V26.75C11.75 27.1478 11.908 27.5294 12.1893 27.8107C12.4706 28.092 12.8522 28.25 13.25 28.25H17.75C18.1478 28.25 18.5294 28.092 18.8107 27.8107C19.092 27.5294 19.25 27.1478 19.25 26.75V22.25C19.25 21.8522 19.092 21.4706 18.8107 21.1893C18.5294 20.908 18.1478 20.75 17.75 20.75ZM26.75 20.75H22.25C21.8522 20.75 21.4706 20.908 21.1893 21.1893C20.908 21.4706 20.75 21.8522 20.75 22.25V26.75C20.75 27.1478 20.908 27.5294 21.1893 27.8107C21.4706 28.092 21.8522 28.25 22.25 28.25H26.75C27.1478 28.25 27.5294 28.092 27.8107 27.8107C28.092 27.5294 28.25 27.1478 28.25 26.75V22.25C28.25 21.8522 28.092 21.4706 27.8107 21.1893C27.5294 20.908 27.1478 20.75 26.75 20.75Z"
                fill="#6A6F79"
              />
            </svg>
            <span>Dashboard</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex flex-col items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
          >
            <svg
              width="40"
              height="40"
              viewBox="0 0 40 40"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <rect width="40" height="40" rx="6" fill="#115934" />
              <path
                d="M28.2901 11.7125C27.3536 10.7761 26.0834 10.25 24.759 10.25C23.4346 10.25 22.1645 10.7761 21.2279 11.7125L11.7123 21.2272C10.7955 22.1676 10.2862 23.4313 10.2945 24.7446C10.3029 26.0579 10.8284 27.315 11.7571 28.2436C12.6858 29.1722 13.943 29.6975 15.2563 29.7057C16.5696 29.7139 17.8333 29.2044 18.7736 28.2875L28.2901 18.7728C29.2248 17.8357 29.7497 16.5662 29.7497 15.2426C29.7497 13.9191 29.2248 12.6496 28.2901 11.7125ZM27.2289 17.7125L22.4711 22.4694L17.5314 17.5306L22.2892 12.7728C22.9468 12.1303 23.8312 11.7731 24.7506 11.7784C25.6699 11.7838 26.5501 12.1514 27.2002 12.8015C27.8503 13.4516 28.2179 14.3317 28.2232 15.2511C28.2286 16.1704 27.8713 17.0548 27.2289 17.7125ZM25.7823 15.7194C25.8521 15.789 25.9074 15.8717 25.9451 15.9628C25.9829 16.0538 26.0023 16.1514 26.0023 16.25C26.0023 16.3485 25.9829 16.4461 25.9451 16.5372C25.9074 16.6282 25.8521 16.711 25.7823 16.7806L23.5323 19.0306C23.4626 19.1002 23.3799 19.1554 23.2889 19.1931C23.1979 19.2308 23.1003 19.2501 23.0018 19.2501C22.9033 19.25 22.8058 19.2306 22.7148 19.1928C22.6238 19.1551 22.5412 19.0998 22.4715 19.0301C22.4019 18.9605 22.3467 18.8777 22.309 18.7867C22.2714 18.6957 22.252 18.5982 22.2521 18.4997C22.2521 18.4012 22.2716 18.3036 22.3093 18.2126C22.347 18.1216 22.4023 18.039 22.472 17.9694L24.722 15.7194C24.8626 15.5788 25.0533 15.4999 25.2522 15.4999C25.451 15.4999 25.6417 15.5788 25.7823 15.7194Z"
                fill="white"
              />
            </svg>
            <span>Products</span>
          </a>
        </li>
      </ul>
    </div>
  </aside>

  <div class="p-4 sm:ml-[110px]">
    <slot></slot>
    <!-- <div
      class="p-4 border-2 border-gray-200 border-dashed rounded-lg dark:border-gray-700"
    >
      <div class="grid grid-cols-3 gap-4 mb-4">
        <div
          class="flex items-center justify-center h-24 rounded bg-gray-50 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center h-24 rounded bg-gray-50 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center h-24 rounded bg-gray-50 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
      </div>
      <div
        class="flex items-center justify-center h-48 mb-4 rounded bg-gray-50 dark:bg-gray-800"
      >
        <p class="text-2xl text-gray-400 dark:text-gray-500">
          <svg
            class="w-3.5 h-3.5"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 18 18"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 1v16M1 9h16"
            />
          </svg>
        </p>
      </div>
      <div class="grid grid-cols-2 gap-4 mb-4">
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
      </div>
      <div
        class="flex items-center justify-center h-48 mb-4 rounded bg-gray-50 dark:bg-gray-800"
      >
        <p class="text-2xl text-gray-400 dark:text-gray-500">
          <svg
            class="w-3.5 h-3.5"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 18 18"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 1v16M1 9h16"
            />
          </svg>
        </p>
      </div>
      <div class="grid grid-cols-2 gap-4">
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
        <div
          class="flex items-center justify-center rounded bg-gray-50 h-28 dark:bg-gray-800"
        >
          <p class="text-2xl text-gray-400 dark:text-gray-500">
            <svg
              class="w-3.5 h-3.5"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 18 18"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 1v16M1 9h16"
              />
            </svg>
          </p>
        </div>
      </div>
    </div> -->
  </div>
</template>

<script setup></script>
