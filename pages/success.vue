<template>
    <MainLayout>
        <div id="SuccessPage" class="mt-4 max-w-[1200px] mx-auto px-2 min-h-[50vh]">
            <div class="bg-white w-full p-6 min-h-[150px]">
                <div class="flex items-center text-xl">
                    <Icon name="clarity:success-standard-line" color="#5FCB04" size="35"/>
                    <span class="pl-4">Order Successful</span>
                </div>
                <p class="text-sm pl-[50px]">Thank you! We've received your order.</p>
                <p class="text-sm pl-[50px]">
                    You can view all your orders<NuxtLink 
                            to="/orders"
                            class="
                                w-full 
                                text-[#FD374F] 
                                font-semibold 
                                p-1.5 
                                rounded-full
                                mt-4
                            "
                        >here
                        </NuxtLink>
                </p>
            </div>
        </div>
    </MainLayout>
</template>

<script setup>
import MainLayout from '~/layouts/MainLayout.vue';
import { useUserStore } from '~/stores/user';
const userStore = useUserStore()

onMounted(() => {
    setTimeout(() => userStore.isLoading = false, 300)
})
</script>