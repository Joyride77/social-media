<script setup>
import { ref } from "vue";
import InputTextarea from "@/Components/InputTextarea.vue";
import { useForm, usePage } from "@inertiajs/vue3";

const authUser = usePage().props.auth.user;

const newPost = ref({
    id: null,
    body: "",
    user: authUser,
});

defineProps({
    group: {
        type: Object,
        default: null,
    },
});

const postCreating = ref(false);
const newPostForm = useForm({
    body: "",
});

function submit(params) {
    newPostForm.post(route("post.create"), {
        onSuccess: () => {
            newPostForm.reset();
        },
    });
}
</script>

<template>
    <div class="p-4 bg-white rounded-lg border mb-3">
        <InputTextarea
            @click="postCreating = true"
            v-model="newPostForm.body"
            class="mb-3 w-full"
            rows="1"
            placeholder="Click here to create new post"
        />

        <div v-if="postCreating" class="flex gap-2 justify-between">
            <button
                type="submit"
                class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 relative"
            >
                Attach files
                <input
                    type="file"
                    class="absolute left-0 top-0 right-0 bottom-0 opacity-0"
                />
            </button>
            <button
                @click="submit"
                type="submit"
                class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
            >
                Submit
            </button>
        </div>
    </div>
</template>
