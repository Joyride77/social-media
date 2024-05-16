<script setup>
import { ref } from "vue";
import PostItem from "./PostItem.vue";
import PostModal from "./PostModal.vue";

defineProps({
    posts: Array,
});

const showEditModal = ref(false);
const editPost = ref({});

function openEditModal(post) {
    editPost.value = post;
    showEditModal.value = true;
}

const post1 = {
    user: {
        id: 1,
        avatar: "https://picsum.photos/200",
        name: "John Smith",
    },
    group: null,
    attachment: [
        {
            id: 1,
            name: "test.png",
            url: "https://picsum.photos/1000",
            mime: "image/png",
        },
        {
            id: 2,
            name: "test2.png",
            url: "https://picsum.photos/1000",
            mime: "image/png",
        },
        {
            id: 3,
            name: "MyDocument.docx",
            url: "#",
            mime: "application/msword",
        },
    ],
    body: `
        <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>

        <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
    `,
    created_at: "2024-11-19 15:12",
};
</script>

<template>
    <div class="overflow-auto">
        <PostItem
            v-for="post of posts"
            :key="post.id"
            :post="post"
            @editClick="openEditModal"
        />

        <PostModal :post="editPost" v-model="showEditModal" />
    </div>
</template>
