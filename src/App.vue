<script setup>
// import { onMounted } from "vue";
// import { initModals } from "flowbite";

// initialize components based on data attribute selectors
// onMounted(() => {
//   initModals();
// });

import { ref } from "vue";

const showModal = ref(false);
const newNote = ref("");
const notes = ref([]);
const errorMessage = ref("")

function getRandomColor() {
  return "hsl(" + Math.random() * 360 + ", 100%, 75%)";
}


  const addNote = ()=>{
    if (newNote.value.length < 10) {
      return errorMessage.value = "Your text must be upto 10 characters"
    }

  notes.value.push({
    id: Math.floor(Math.random()* 10000000),
    text: newNote.value,
    date: new Date(),
    backgroundColor: getRandomColor()
})
  showModal.value = false;
  newNote.value = "";
  errorMessage.value = ""
}




</script>


<template>
  <main>
    <div class="w-[1000px] mx-auto">
      <div class="flex justify-between p-4">
        <h2 class="text-3xl">Notes </h2>

        <button @click="showModal = true" 
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
          <div v-for="note in notes" :key="note.id" :style="{backgroundColor:note.backgroundColor}"
                class="w-56 h-56 relative p-6 border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
              >
            <p
              class="font-normal text-gray-700 dark:text-gray-400 text-sm"
            >{{note.text}}</p>
            <p class="absolute inset-x-0 bottom-0 h-8 text-gray-700 pl-6 text-xs">{{note.date.toLocaleDateString("en-UK")}}</p>
          </div>

      </div>

    
    </div>

    <!-- Modal  -->

  <!-- Main modal -->
  <div v-show="showModal"  class="fixed z-50 w-full bg-slate-400 p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-modal md:h-full">
      <div class="relative w-full h-full max-w-2xl mx-auto my-32">
          <!-- Modal content -->
          <div class="relative bg-white rounded-lg shadow dark:bg-gray-700 mx-auto">
              <!-- Modal header -->
              <div class="flex items-start justify-between p-4 border-b rounded-t dark:border-gray-600">
                  <h3 class="text-xl font-semibold text-gray-900 dark:text-white">
                     Add New Note
                  </h3>
                  <button @click="showModal = false" type="button" class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-600 dark:hover:text-white" >
                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>  
                  </button>
              </div>
              <!-- Modal body -->
              <div class="p-6">
                  <textarea cols="64" rows="8" v-model.trim="newNote"></textarea>
                  <p v-if="errorMessage">{{ errorMessage }}</p>
              </div>
              <!-- Modal footer -->
              <div class="flex justify-end pr-6 pb-8 border-gray-200 rounded-b dark:border-gray-600">
                  <button @click="addNote"  type="button" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Add Note</button>
              </div>
          </div>
      </div>
  </div>

    <!-- end of modla -->
  </div>
  <!-- EndCards -->

  
   
   



     




  </main>
</template>

