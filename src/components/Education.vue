<template>
    <div class="m-30" v-for="edu in eduction" :key="edu.institution">
        <p class="main-content-heading">{{ edu.institution }}</p>
        <p>{{ edu.degree }} | {{ edu.dateRange }}</p>
    </div>
</template>

<script>
export default {
    name: "Education",
    data() {
        return {
            eduction: [
                { institution: "Northern Arizona University", degree: "Master of Science - MS, Computer Science", dateRange: "2021 ~ 2022" },
                { institution: "Visvesvaraya Technological University", degree: "Bachelor of Technology - BTech, Computer Science", dateRange: "2015 ~ 2019" }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.main-content-heading{
    color: $content-heading-color;
}

</style>