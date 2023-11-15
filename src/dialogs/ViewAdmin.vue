<template>
    <button type="button" @click="openModal" class="rounded-full">
        <i class="fa-regular fa-eye fa-lg text-gray-400"></i>
    </button>

    <TransitionRoot appear :show="isOpen" as="template">
        <Dialog as="div" @close="closeModal" class="relative z-10">
            <TransitionChild as="template" enter="duration-300 ease-out" enter-from="opacity-0" enter-to="opacity-100"
                leave="duration-200 ease-in" leave-from="opacity-100" leave-to="opacity-0">
                <div class="fixed inset-0 bg-black/25" />
            </TransitionChild>

            <div class="fixed inset-0 overflow-y-auto">
                <div class="flex min-h-full items-center justify-center p-4 text-center">
                    <TransitionChild as="template" enter="duration-300 ease-out" enter-from="opacity-0 scale-95"
                        enter-to="opacity-100 scale-100" leave="duration-200 ease-in" leave-from="opacity-100 scale-100"
                        leave-to="opacity-0 scale-95">
                        <DialogPanel class="panel">
                            <div class="flex items-start justify-between p-4 rounded-t dark:border-gray-600">
                                <h3 class="text-xl font-semibold text-gray-900 dark:text-white">
                                    عرض المشرف
                                </h3>
                                <button type="button" @click="closeModal"
                                    class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ml-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white">
                                    <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
                                        viewBox="0 0 14 14">
                                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                            stroke-width="2" d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6" />
                                    </svg>
                                </button>
                            </div>
                            <div class="mt-2">

                                <div class="p-6 space-y-6">
                                    <header class="flex flex-col justify-center items-center">
                                        <img class="lg:w-full w-full lg:h-64 h-64 object-cover object-center rounded"
                                            src="https://stackdiary.com/140x100.png" />
                                    </header>
                                    <div class="mt-2">
                                        <div class="mt-5 grid grid-cols-1 gap-x-6 gap-y-8 sm:grid-cols-6">
                                            <div class="sm:col-span-3">
                                                <label for="going-from"
                                                    class="block text-sm font-medium leading-6 text-gray-900">اسم
                                                    المشرف</label>
                                                <div class="mt-2">
                                                    <div
                                                        class="rounded-lg border border-gray-300 shadow-sm bg-slate-300 text-black py-1.5">
                                                        <p class="font-medium ml-2">Carfour</p>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="sm:col-span-3">
                                                <label for="arrival-in"
                                                    class="block text-sm font-medium leading-6 text-gray-900">رقم
                                                    المشرف</label>
                                                <div class="mt-2">
                                                    <div
                                                        class="rounded-lg border border-gray-300 shadow-sm bg-slate-300 text-black py-1.5">
                                                        <p class="font-medium ml-2">1234343</p>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>

                                <div class="flex items-center p-6 space-x-2 rounded-b dark:border-gray-600">
                                    <button @click="closeModal" type="button" class="btn ml-auto">
                                        غلق</button>
                                </div>
                            </div>
                        </DialogPanel>
                    </TransitionChild>
                </div>
            </div>
        </Dialog>
    </TransitionRoot>
</template>
  
<script setup>
import { ref } from 'vue'
import { TransitionRoot, TransitionChild, Dialog, DialogPanel } from '@headlessui/vue'

const isOpen = ref(false)

const closeModal = () => {
    isOpen.value = false
}
const openModal = () => {
    isOpen.value = true
}
</script>