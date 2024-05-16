<script setup>
import { Head, Link } from "@inertiajs/vue3";
import GroupItem from "@/Components/app/Group/GroupItem.vue";
import TextInput from "@/Components/TextInput.vue";
import GroupList from "@/Components/app/Group/GroupList.vue";
import FollowingList from "@/Components/app/Following/FollowingList.vue";
import PostList from "@/Components/app/Post/PostList.vue";
import CreatePost from "@/Components/app/Post/CreatePost.vue";
import AuthenticatedLayout from "@/Layouts/AuthenticatedLayout.vue";

defineProps({
    posts: Object,
});
</script>

<template>
    <Head title="Social Media Website" />

    <AuthenticatedLayout>
        <div class="grid lg:grid-cols-12 gap-3 p-4 h-full">
            <div class="lg:col-span-3 lg:order-1 h-full overflow-hidden">
                <GroupList />
            </div>
            <div class="lg:col-span-3 lg:order-3 h-full overflow-hidden">
                <FollowingList />
            </div>
            <div
                class="lg:col-span-6 lg:order-2 h-full overflow-hidden flex flex-col"
            >
                <CreatePost />
                <PostList :posts="posts.data" class="flex-1" />
            </div>
        </div>
    </AuthenticatedLayout>
</template>
