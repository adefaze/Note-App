<script setup>
import { onMounted } from "vue";
import { initModals } from "flowbite";

// initialize components based on data attribute selectors
onMounted(() => {
  initModals();
});
</script>


<template>
  <main>
    <div class="w-[1000px] mx-auto">
      <div class="flex justify-between p-4">
        <h2 class="text-3xl">Notes</h2>

        <button
          id="button"
          data-modal-toggle="modal"
          data-modal-target="modal"
          type="button"
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
        class="w-56 h-56 relative  p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
      >
        <p
          class="font-normal text-gray-700 dark:text-gray-400 text-sm"
        >Here are the biggest enterprise technology acquisitions of 2021 </p>
        <p class="absolute inset-x-0 bottom-0  h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
      </div>

      <div
        class="w-56 h-56 relative  p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
      >
        <p
          class="font-normal text-gray-700 dark:text-gray-400 text-sm"
        >Here are the biggest enterprise technology acquisitions of 2021 </p>
        <p class="absolute inset-x-0 bottom-0  h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
      </div>

      <div
        class="w-56 h-56 relative  p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
      >
        <p
          class="font-normal text-gray-700 dark:text-gray-400 text-sm"
        >Here are the biggest enterprise technology acquisitions of 2021 </p>
        <p class="absolute inset-x-0 bottom-0  h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
      </div>

      <div
        class="w-56 h-56 relative  p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
      >
        <p
          class="font-normal text-gray-700 dark:text-gray-400 text-sm"
        >Here are the biggest enterprise technology acquisitions of 2021 </p>
        <p class="absolute inset-x-0 bottom-0  h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
      </div>

      <div
        class="w-56 h-56 relative  p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
      >
        <p
          class="font-normal text-gray-700 dark:text-gray-400 text-sm"
        >Here are the biggest enterprise technology acquisitions of 2021 </p>
        <p class="absolute inset-x-0 bottom-0  h-8 text-gray-700 pl-6 text-xs">12/06/2023</p>
      </div>
      
    </div>
  </div>
  <!-- EndCards -->

  <!-- Modal-->
  <div
      id="modal"
      tabindex="-1"
      aria-hidden="true"
      class="fixed top-0 left-0 right-0 z-50 hidden w-full p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-modal md:h-full"
    >
      <div class="relative w-full h-full max-w-2xl md:h-auto">
        <!-- Modal content -->
        <div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
          <!-- Modal header -->
          <div class="flex items-start justify-between p-5 border-b rounded-t dark:border-gray-600">
            <h3 class="text-xl font-semibold text-gray-900 lg:text-2xl dark:text-white">Add New Note</h3>
            <button
              id="closeButton"
              data-modal-hide="modal"
              type="button"
              class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white"
            >
              <svg
                class="w-5 h-5"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                />
              </svg>
            </button>
          </div>
          <!-- Modal body -->
          <div class="p-6">
            <textarea cols="65" rows="5"></textarea>
          </div>
          <!-- Modal footer -->
          <div class="text-right p-6 rounded-b">
            <button
              type="button"
              class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
            >Add Note</button>
          </div>
        </div>
      </div>
    </div>
    </div>
  </main>


</template>

