<script setup>
import TextInput from "@/Components/TextInput.vue";
import { ref } from "vue";
import FollowingItem from "./FollowingItem.vue";

const searchKeyword = ref('')

</script>

<template>
    <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full mt-4" />
    <div class="mt-3 h-[200px] lg:flex-1 overflow-auto">
        <div v-if="false" class="text-gray-400 text-center p-3">
            <p>You are have no friends added</p>
        </div>
        <div v-else>
            <FollowingItem image="https://picsum.photos/100" title="John Doe"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="Alex Max"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="John Doe"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="Alex Max"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="John Doe"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="Alex Max"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="John Doe"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="Alex Max"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="John Doe"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="Alex Max"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="John Doe"
                description="Lorem ipsum dolor sit amet, elit." />
            <FollowingItem image="https://picsum.photos/100" title="Alex Max"
                description="Lorem ipsum dolor sit amet, elit." />
        </div>

    </div>
</template>

<style scoped></style>
