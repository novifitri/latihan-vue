<template>
  <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
    <div class="flex justify-end mt-4 pb-4 bg-white dark:bg-gray-900">
      <label for="table-search" class="sr-only">Search</label>
      <div class="relative mt-1">
        <div
          class="absolute inset-y-0 rtl:inset-r-0 start-0 flex items-center ps-3 pointer-events-none"
        >
          <svg
            class="w-4 h-4 text-gray-500 dark:text-gray-400"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 20 20"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
            />
          </svg>
        </div>
        <input
          type="text"
          id="table-search"
          class="block pt-2 ps-10 text-sm text-gray-900 border border-gray-300 rounded-lg w-80 bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
          placeholder="Search for items"
        />
      </div>
    </div>
    <table
      class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400"
    >
      <thead
        class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
      >
        <tr>
          <th scope="col" class="px-6 py-3">No</th>
          <th scope="col" class="px-6 py-3">Title</th>
          <th scope="col" class="px-6 py-3">Description</th>
          <th scope="col" class="px-6 py-3">category</th>
          <th scope="col" class="px-6 py-3">Price</th>
          <th scope="col" class="px-6 py-3">Stock</th>
        </tr>
      </thead>
      <tbody>
        <tr v-if="isLoading">
          <div role="status">
            <svg
              aria-hidden="true"
              class="w-8 h-8 text-gray-200 animate-spin dark:text-gray-600 fill-blue-600"
              viewBox="0 0 100 101"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z"
                fill="currentColor"
              />
              <path
                d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z"
                fill="currentFill"
              />
            </svg>
            <span class="sr-only">Loading...</span>
          </div>
        </tr>
        <tr
          v-else
          v-for="product in products"
          :key="product.id"
          class="odd:bg-white odd:dark:bg-gray-900 even:bg-gray-50 even:dark:bg-gray-800 border-b dark:border-gray-700"
        >
          <th
            scope="row"
            class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white"
          >
            {{ product.id }}
          </th>
          <td class="px-6 py-4">{{ product.title }}</td>
          <td class="px-6 py-4">
            {{ product.description }}
          </td>
          <td class="px-6 py-4">{{ product.category }}</td>
          <td class="px-6 py-4">{{ product.price }}</td>
          <td class="px-6 py-4">{{ product.stock }}</td>
        </tr>
      </tbody>
    </table>
  </div>
  <!-- Pagination start -->
  <div v-if="!isLoading" class="flex justify-between mt-[14px]">
    <div class="flex gap-2 items-center">
      <select v-model="limit">
        <option value="10">10</option>
        <option value="20">20</option>
        <option value="50">50</option>
        <option value="100">100</option>
      </select>
      <p>Showing {{ start + 1 }} to {{ end }} of {{ total }} items</p>
    </div>
    <div>
      <button
        @click="prevPage"
        type="button"
        class="text-gray-900 border border-gray-300 hover:bg-gray-300 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      >
        <svg
          width="21"
          height="20"
          viewBox="0 0 21 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M6.30795 10.4422L12.558 16.6922C12.616 16.7503 12.685 16.7963 12.7608 16.8277C12.8367 16.8592 12.918 16.8753 13.0001 16.8753C13.0823 16.8753 13.1636 16.8592 13.2395 16.8277C13.3153 16.7963 13.3843 16.7503 13.4423 16.6922C13.5004 16.6341 13.5465 16.5652 13.5779 16.4893C13.6093 16.4134 13.6255 16.3321 13.6255 16.25C13.6255 16.1679 13.6093 16.0866 13.5779 16.0107C13.5465 15.9348 13.5004 15.8659 13.4423 15.8078L7.63373 10L13.4423 4.19219C13.5596 4.07491 13.6255 3.91585 13.6255 3.75C13.6255 3.58415 13.5596 3.42509 13.4423 3.30781C13.3251 3.19054 13.166 3.12465 13.0001 3.12465C12.8343 3.12465 12.6752 3.19054 12.558 3.30781L6.30795 9.55781C6.24984 9.61586 6.20374 9.68479 6.17229 9.76066C6.14084 9.83654 6.12465 9.91787 6.12465 10C6.12465 10.0821 6.14084 10.1635 6.17229 10.2393C6.20374 10.3152 6.24984 10.3841 6.30795 10.4422Z"
            fill="#9E9D9D"
          />
        </svg>

        <span class="sr-only">Icon description</span>
      </button>
      <button
        type="button"
        @click="nextPage"
        class="text-gray-900 border border-gray-300 hover:bg-gray-300 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm p-2.5 text-center inline-flex items-center me-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      >
        <svg
          width="20"
          height="20"
          viewBox="0 0 20 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M14.192 10.4422L7.94205 16.6922C7.88398 16.7503 7.81504 16.7963 7.73917 16.8277C7.6633 16.8592 7.58198 16.8753 7.49986 16.8753C7.41774 16.8753 7.33642 16.8592 7.26055 16.8277C7.18468 16.7963 7.11574 16.7503 7.05767 16.6922C6.9996 16.6341 6.95354 16.5652 6.92211 16.4893C6.89069 16.4134 6.87451 16.3321 6.87451 16.25C6.87451 16.1679 6.89069 16.0866 6.92211 16.0107C6.95354 15.9348 6.9996 15.8659 7.05767 15.8078L12.8663 10L7.05767 4.19219C6.9404 4.07491 6.87451 3.91585 6.87451 3.75C6.87451 3.58415 6.9404 3.42509 7.05767 3.30781C7.17495 3.19054 7.33401 3.12465 7.49986 3.12465C7.66571 3.12465 7.82477 3.19054 7.94205 3.30781L14.192 9.55781C14.2502 9.61586 14.2963 9.68479 14.3277 9.76066C14.3592 9.83654 14.3754 9.91787 14.3754 10C14.3754 10.0821 14.3592 10.1635 14.3277 10.2393C14.2963 10.3152 14.2502 10.3841 14.192 10.4422Z"
            fill="#0A0A0A"
          />
        </svg>

        <span class="sr-only">Icon description</span>
      </button>
    </div>
  </div>
</template>

<script>
import { onMounted, ref, watch } from 'vue'

export default {
  setup() {
    const start = ref(0)
    const end = ref(10)
    const limit = ref(10)
    const isLoading = ref(true)
    const total = ref(0)
    const products = ref(null)

    const fetchData = () => {
      isLoading.value = true
      fetch(
        `https://dummyjson.com/products?limit=${limit.value}&skip=${start.value}`
      )
        .then((res) => res.json())
        .then((data) => {
          isLoading.value = false
          products.value = data.products
          total.value = data.total
          end.value = data.skip + data.products?.length
        })
    }
    const prevPage = () => {
      if (start.value !== 0) {
        start.value = start.value - 10
      }
    }
    const nextPage = () => {
      if (end.value < total.value) {
        start.value = end.value
      }
    }
    onMounted(() => {
      fetchData()
    })
    watch([limit, start], () => {
      fetchData()
    })

    return {
      start,
      end,
      limit,
      isLoading,
      products,
      fetchData,
      prevPage,
      nextPage,
      total,
    }
  },
}
</script>

<style lang="scss" scoped></style>
