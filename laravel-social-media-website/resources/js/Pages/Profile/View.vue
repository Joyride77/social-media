<script setup>
import { usePage } from "@inertiajs/vue3";
import { computed, ref } from "vue";
import { TabGroup, TabList, Tab, TabPanels, TabPanel } from "@headlessui/vue";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";
import TabItem from "./Partials/TabItem.vue";
import Edit from "./Edit.vue";
import PrimaryButton from "@/Components/PrimaryButton.vue";

const authUser = usePage().props.auth.user;

const props = defineProps({
    mustVerifyEmail: {
        type: Boolean,
    },
    status: {
        type: String,
    },
    user: {
        type: Object,
    },
});

const isMyProfile = computed(() => authUser && authUser.id === props.user.id);
</script>

<template>
    <AuthenticatedLayout>
        <div class="w-[768px] mx-auto h-full overflow-auto">
            <div class="relative bg-white">
                <!--Cover-->
                <img
                    src="https://iwritingsolutions.com/wp-content/uploads/2022/05/starry-sky-night-dark-wallpaper-preview-1.jpg"
                    class="w-full h-[300px] object-cover"
                />

                <div class="flex">
                    <!--Avatar-->
                    <img
                        src="https://www.thesprucepets.com/thmb/A5Rkkt4HDWLAtUOk4gYybcX02mM=/1080x0/filters:no_upscale():strip_icc()/30078352_448703938920062_6275637137232625664_n-5b0de8c443a1030036f9e15e.jpg"
                        class="ml-[48px] -mt-[64px] w-[128px] h-[128px] rounded-full"
                    />

                    <!--User information-->
                    <div class="flex justify-between items-center flex-1 p-4">
                        <h2 class="font-bold text-lg">{{ user.name }}</h2>
                        <PrimaryButton v-if="isMyProfile">
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                fill="none"
                                viewBox="0 0 24 24"
                                stroke-width="1.5"
                                stroke="currentColor"
                                class="w-4 h-4 mr-2 mt-[-2px]"
                            >
                                <path
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    d="m16.862 4.487 1.687-1.688a1.875 1.875 0 1 1 2.652 2.652L10.582 16.07a4.5 4.5 0 0 1-1.897 1.13L6 18l.8-2.685a4.5 4.5 0 0 1 1.13-1.897l8.932-8.931Zm0 0L19.5 7.125M18 14v4.75A2.25 2.25 0 0 1 15.75 21H5.25A2.25 2.25 0 0 1 3 18.75V8.25A2.25 2.25 0 0 1 5.25 6H10"
                                />
                            </svg>

                            Edit Button
                        </PrimaryButton>
                    </div>
                </div>
            </div>
            <div class="border-t">
                <TabGroup>
                    <TabList class="flex bg-white">
                        <Tab
                            v-if="isMyProfile"
                            v-slot="{ selected }"
                            as="template"
                        >
                            <TabItem text="About" :selected="selected" />
                        </Tab>
                        <Tab v-slot="{ selected }" as="template">
                            <TabItem text="Posts" :selected="selected" />
                        </Tab>
                        <Tab v-slot="{ selected }" as="template">
                            <TabItem text="Followers" :selected="selected" />
                        </Tab>
                        <Tab v-slot="{ selected }" as="template">
                            <TabItem text="Followings" :selected="selected" />
                        </Tab>
                        <Tab v-slot="{ selected }" as="template">
                            <TabItem text="Photos" :selected="selected" />
                        </Tab>
                    </TabList>

                    <TabPanels class="mt-2">
                        <TabPanel
                            v-if="isMyProfile"
                            :key="about"
                            class="rounded-xl shadow"
                        >
                            <Edit
                                :must-verify-email="mustVerifyEmail"
                                :status="status"
                            />
                        </TabPanel>
                    </TabPanels>

                    <TabPanels class="mt-2">
                        <TabPanel
                            :key="posts"
                            class="rounded-xl bg-white p-3 shadow"
                        >
                            Post Content
                        </TabPanel>
                    </TabPanels>

                    <TabPanels class="mt-2">
                        <TabPanel
                            :key="followers"
                            class="rounded-xl bg-white p-3 shadow"
                        >
                            Followers
                        </TabPanel>
                    </TabPanels>

                    <TabPanels class="mt-2">
                        <TabPanel
                            :key="followings"
                            class="rounded-xl bg-white p-3 shadow"
                        >
                            Followings
                        </TabPanel>
                    </TabPanels>

                    <TabPanels class="mt-2">
                        <TabPanel
                            :key="photos"
                            class="rounded-xl bg-white p-3 shadow"
                        >
                            Photos
                        </TabPanel>
                    </TabPanels>
                </TabGroup>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
