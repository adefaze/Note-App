<script setup>
import { onMounted } from "vue";
// import { initModals } from "flowbite";

// initialize components based on data attribute selectors
// onMounted(() => {
//   initModals();
// });

import { ref } from "vue";

const showModal = ref(false);
</script>


<template>
  <main>
    <div class="w-[1000px] mx-auto">
      <div class="flex justify-between p-4">
        <h2 class="text-3xl">Notes</h2>

        <button
          @click="showModal = true"
          data-modal-target="staticModal" data-modal-toggle="staticModal"
          class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-full text-sm p-2.5 text-center inline-flex items-center mr-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
        >
          <svg
            aria-hidden="true"
            class="w-4 h-4"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
              clip-rule="evenodd"
            />
          </svg>
          <span class="sr-only">Icon description</span>
        </button>
      </div>
      <!-- Cards -->
      <div class="container">
        <div class="flex flex-wrap gap-8">
          <div
            class="w-56 h-56 relative p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
          >
            <p
              class="font-normal text-gray-700 dark:text-gray-400 text-sm"
            >Here are the biggest enterprise technology acquisitions of 2021</p>
            <p class="absolute inset-x-0 bottom-0 h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
          </div>

          <div
            class="w-56 h-56 relative p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
          >
            <p
              class="font-normal text-gray-700 dark:text-gray-400 text-sm"
            >Here are the biggest enterprise technology acquisitions of 2021</p>
            <p class="absolute inset-x-0 bottom-0 h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
          </div>

          <div
            class="w-56 h-56 relative p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
          >
            <p
              class="font-normal text-gray-700 dark:text-gray-400 text-sm"
            >Here are the biggest enterprise technology acquisitions of 2021</p>
            <p class="absolute inset-x-0 bottom-0 h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
          </div>

          <div
            class="w-56 h-56 relative p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
          >
            <p
              class="font-normal text-gray-700 dark:text-gray-400 text-sm"
            >Here are the biggest enterprise technology acquisitions of 2021</p>
            <p class="absolute inset-x-0 bottom-0 h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
          </div>

          <div
            class="w-56 h-56 relative p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
          >
            <p
              class="font-normal text-gray-700 dark:text-gray-400 text-sm"
            >Here are the biggest enterprise technology acquisitions of 2021</p>
            <p class="absolute inset-x-0 bottom-0 h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
          </div>
        </div>
      </div>
      <!-- EndCards -->

     
    </div>

     




  </main>
</template>

