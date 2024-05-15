<script setup>
import TextInput from "@/Components/TextInput.vue";
import GroupItem from "@/Components/app/Group/GroupItem.vue";
import { ref } from "vue";

const searchKeyword = ref('')

</script>

<template>
    <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full mt-4" />
    <div class="mt-3 h-[200px] lg:flex-1 overflow-auto">
        <div v-if="false" class="text-gray-400 text-center p-3">
            <p>You are not joined to any group</p>
        </div>
        <div v-else>
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Laravel Dev"
                description="Lorem ipsum dolor sit amet, elit." />
            <GroupItem image="https://picsum.photos/100" title="Vue Dev"
                description="Lorem ipsum dolor sit amet, elit." />
        </div>

    </div>
</template>

<style scoped></style>
