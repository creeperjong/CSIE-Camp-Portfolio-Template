<script setup>
import Typing from "../components/Typing.vue";
import Project from "../components/Project.vue";

const projects = [
    {
        title: "Project A",
        description: "...",
        image: "url..."
    },
    {
        title: "Project B",
        description: "...",
        image: "url..."
    }
];

</script>
<template>
    <div class="h-full w-full px-8 pt-16 sm:px-12 sm:pt-20 lg:px-16 lg:pt-24">
        <Typing text="My Projects" class="block text-2xl sm:text-3xl lg:text-4xl" />
        <div class="py-2">
            <Project
                v-for="project in projects"
                :key="project"
                :name = "project.title"
                :description = "project.description"
                :image = "project.image"
            >
            </Project>
        </div>
    </div>
</template>
