<template>
    <div class="bg-white">
        <div class="px-6 py-4 grid gap-3 md:flex md:justify-between md:items-center">
            <div class="sm:col-span-2 md:grow">
                <div class="flex justify-end gap-x-2">
                    <div class="relative inline-block">
                        <AddCategory />
                    </div>
                </div>
            </div>
        </div>

        <div class="mx-auto max-w-full px-4 sm:px-6 lg:max-w-7xl lg:px-8">
            <div class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
                <div v-for="product in products" :key="product.id" class="group relative transit">
                    <button type="button" class="absolute top-2 right-2 mx-3 mt-3 z-10">
                        <i class="fa-solid fa-trash" style="color: #F31559"></i>
                    </button>
                    <div
                        class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80">
                        <img :src="product.imageSrc" class="h-full w-full object-cover object-center lg:h-full lg:w-full" />
                    </div>
                    <div class="mt-4 flex justify-between">
                        <div>
                            <h3 class="text-sm text-gray-700">
                                <router-link :to="product.route">
                                    <span aria-hidden="true" class="absolute inset-0" />
                                    {{ product.name }}
                                </router-link>
                            </h3>
                            <p class="mt-1 text-sm text-gray-500">{{ product.color }}</p>
                        </div>
                        <p class="text-sm font-medium text-gray-900">{{ product.price }}</p>
                    </div>
                    <div class="mt-8">
                        <!-- <button type="button" class="">
                            <i class="fa-solid fa-pen-to-square"></i>
                        </button> -->
                        <EditCategory />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script setup>
import AddCategory from '../dialogs/AddCategory.vue';
import EditCategory from '../dialogs/EditCategory.vue';

const products = [
    {
        id: 1,
        name: 'Basic Tee',
        route: '',
        imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-01.jpg',
        price: '$35',
        color: 'Black',
    },
    {
        id: 1,
        name: 'Basic Tee',
        route: '',
        imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-01.jpg',
        price: '$35',
        color: 'Black',
    },
    {
        id: 1,
        name: 'Basic Tee',
        route: '',
        imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-01.jpg',
        price: '$35',
        color: 'Black',
    },
    {
        id: 1,
        name: 'Basic Tee',
        route: '',
        imageSrc: 'https://tailwindui.com/img/ecommerce-images/product-page-01-related-product-01.jpg',
        price: '$35',
        color: 'Black',
    },
]

const openModal = () => {
    console.log('open modal')
}
</script>