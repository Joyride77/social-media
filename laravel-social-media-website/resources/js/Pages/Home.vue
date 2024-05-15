<script setup>
import { Head, Link } from '@inertiajs/vue3';
import GroupItem from '@/Components/app/Group/GroupItem.vue';
import TextInput from '@/Components/TextInput.vue';
import GroupList from '@/Components/app/Group/GroupList.vue';
import FollowingList from '@/Components/app/Following/FollowingList.vue';
import PostList from '@/Components/app/Post/PostList.vue';
import CreatePost from '@/Components/app/Post/CreatePost.vue';

defineProps({
    posts: Object,
    groups: Array,
    followings: Array
});

</script>

<template>

    <Head title="Social Media Website" />

    <div class="grid grid-cols-12 gap-3 p-4 h-full">
        <div class="col-span-3 py-6">
            <GroupList />
        </div>
        <div class="col-span-6 py-6">
            <CreatePost />
            <PostList />
        </div>
        <div class="col-span-3 py-6">
            <FollowingList />
        </div>

    </div>

</template>
