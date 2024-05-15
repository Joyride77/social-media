<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import FollowingListItems from './FollowingListItems.vue';

defineProps({
    groups: Array
})

</script>

<template>
    <div class="px-3 bg-white rounded border py-3 h-full overflow-hidden">

        <div class="block lg:hidden">
            <Disclosure v-slot="{ open }">
                <DisclosureButton class="w-full">
                    <div class="flex justify-between items-center">
                        <h2 class="text-xl font-bold px-3">My Following</h2>
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                            stroke="currentColor" class="w-6 h-6 transition-all"
                            :class="open ? 'rotate-90 transform' : ''">
                            <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
                        </svg>
                    </div>

                </DisclosureButton>
                <DisclosurePanel>
                    <FollowingListItems />
                </DisclosurePanel>
            </Disclosure>
        </div>

        <div class="h-full overflow-hidden flex-col hidden lg:flex">
            <h2 class="text-xl font-bold">My Following</h2>
            <FollowingListItems />
        </div>

    </div>
</template>

<style scoped></style>
