<template>
  <div class="px-6 py-4 grid gap-3 md:flex md:justify-between md:items-center">
    <div class="sm:col-span-2 md:grow">
      <div class="flex justify-end gap-x-2">
        <div class="relative inline-block">
          <AddMarket />
        </div>
      </div>
    </div>
  </div>

  <div class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8">
    <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
      <div class="flex items-center justify-between pb-4 bg-white mb-4 dark:bg-gray-900">
        <div>
          <button id="dropdownActionButton" data-dropdown-toggle="dropdownAction"
            class="inline-flex items-center text-gray-500 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-lg text-sm px-3 py-1.5 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700"
            type="button">
            منقي
            <i class="fa-solid fa-chevron-down w-2.5 h-2.5 ml-2.5"></i>
          </button>
          <!-- Dropdown menu -->
          <div id="dropdownAction"
            class="z-10 hidden bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700 dark:divide-gray-600">
            <ul class="py-1 text-sm text-gray-700 dark:text-gray-200" aria-labelledby="dropdownActionButton">
              <li>
                <a href="#"
                  class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Approved</a>
              </li>
              <li>
                <a href="#"
                  class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Pending</a>
              </li>
              <li>
                <a href="#"
                  class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Rejected</a>
              </li>
            </ul>
          </div>
        </div>

        <div class="relative">
          <div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
            <i class="fa-solid fa-magnifying-glass w-4 h-4 text-gray-500 dark:text-gray-400"></i>
          </div>
          <input type="text" id="table-search-markets"
            class="block p-2 pl-10 text-sm text-gray-900 border border-gray-300 rounded-lg w-80 bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="البجث عن متجر">
        </div>

      </div>
      <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
        <thead class="text-xs text-gray-700 bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
          <tr>
            <th scope="col" class="p-4">
              <div class="flex items-center">
                <input id="checkbox-all-search" type="checkbox"
                  class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
              </div>
            </th>
            <th scope="col" class="px-6 py-3">
              متجر
            </th>
            <!-- <th scope="col" class="px-6 py-3">
            Position
          </th> -->
            <th scope="col" class="px-6 py-3">
              الحاله
            </th>
            <th scope="col" class="px-6 py-3">
              فعل
            </th>
          </tr>
        </thead>
        <tbody>
          <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 hover:bg-gray-50 dark:hover:bg-gray-600">
            <td class="w-4 p-4">
              <div class="flex items-center">
                <input id="checkbox-table-search-1" type="checkbox"
                  class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
              </div>
            </td>
            <th scope="row" class="flex items-center px-6 py-4 text-gray-900 whitespace-nowrap dark:text-white">
              <img class="w-10 h-10 rounded-full"
                src="https://justfields.com/storage/projects/7M5rV059/hoodie_2_front.jpg">
              <div class="pl-3">
                <div class="text-base font-semibold">Neil Sims</div>
                <div class="font-normal text-gray-500">neil.sims@flowbite.com</div>
              </div>
            </th>
            <!-- <td class="px-6 py-4">
            React Developer
          </td> -->
            <td class="px-6 py-4">
              <div class="flex items-center">
                <div class="h-2.5 w-2.5 rounded-full bg-yellow-300 mr-2"></div>Pending
              </div>
            </td>
            <td class="px-6 py-4">
              <a href="#" class="font-medium text-blue-600 dark:text-blue-500">
                <ActionsDialogsMarket />
              </a>
            </td>
          </tr>

          <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 hover:bg-gray-50 dark:hover:bg-gray-600">
            <td class="w-4 p-4">
              <div class="flex items-center">
                <input id="checkbox-table-search-2" type="checkbox"
                  class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
              </div>
            </td>
            <th scope="row"
              class="flex items-center px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
              <img class="w-10 h-10 rounded-full" src="https://justfields.com/storage/projects/7M5rV059/beanie-2.jpg">
              <div class="pl-3">
                <div class="text-base font-semibold">Bonnie Green</div>
                <div class="font-normal text-gray-500">bonnie@flowbite.com</div>
              </div>
            </th>
            <!-- <td class="px-6 py-4">
            Designer
          </td> -->
            <td class="px-6 py-4">
              <div class="flex items-center">
                <div class="h-2.5 w-2.5 rounded-full bg-green-500 mr-2"></div>Approved
              </div>
            </td>
            <td class="px-6 py-4">
              <a href="#" class="font-medium text-blue-600 dark:text-blue-500">
                <ActionsDialogsMarket />
              </a>
            </td>
          </tr>

          <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 hover:bg-gray-50 dark:hover:bg-gray-600">
            <td class="w-4 p-4">
              <div class="flex items-center">
                <input id="checkbox-table-search-2" type="checkbox"
                  class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
              </div>
            </td>
            <th scope="row"
              class="flex items-center px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
              <img class="w-10 h-10 rounded-full" src="https://justfields.com/storage/projects/7M5rV059/hoodie-22.jpg">
              <div class="pl-3">
                <div class="text-base font-semibold">Jese Leos</div>
                <div class="font-normal text-gray-500">jese@flowbite.com</div>
              </div>
            </th>
            <!-- <td class="px-6 py-4">
            Vue JS Developer
          </td> -->
            <td class="px-6 py-4">
              <div class="flex items-center">
                <div class="h-2.5 w-2.5 rounded-full bg-red-500 mr-2"></div>Rejected
              </div>
            </td>
            <td class="px-6 py-4">
              <a href="#" class="font-medium text-blue-600 dark:text-blue-500">
                <ActionsDialogsMarket />
              </a>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import { initDropdowns } from 'flowbite'
import ActionsDialogsMarket from '../dialogs/ActionsDialogsMarket.vue';
import AddMarket from '../dialogs/AddMarket.vue';

onMounted(() => {
  initDropdowns();
})
</script>