<script setup>
import TextInput from '@/Components/TextInput.vue';
import GroupItem from './GroupItem.vue';
import { ref } from 'vue';

const searchKeyword = ref('')

defineProps({
    groups: Array
})

</script>

<template>
    <div class="px-3">
        <h2 class="text-2xl font-bold px-3 mb-4">My Groups</h2>
        <TextInput :model-value="searchKeyword" placeholder="Type to search" />
        <div class="py-8">
            <div>
                <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                    description="Lorem ipsum dolor sit amet, elit." />
                <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                    description="Lorem ipsum dolor sit amet, elit." />
            </div>

        </div>

    </div>
</template>

<style scoped></style>
