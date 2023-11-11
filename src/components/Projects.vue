<template>
    <div class="projects">
        <div class="sub-project m-30" v-for="project in projects" :key="project.projectName">
            <p class="main-content-heading">{{ project.projectName }}</p>
            <p> - {{ project.projectDescription }}</p>
            <div v-if="project.githubLink && project.websiteLink">
                <p> - Links: <span> <a :href="project.githubLink" target="_blank">[GitHub]</a> |
                        <a :href="project.websiteLink" target="_blank">[Website]</a></span></p>
            </div>
            <div v-else-if="project.githubLink">
                <p> - Link: <span><a :href="project.githubLink" target="_blank">[GitHub]</a></span></p>
            </div>
            <div v-else-if="project.websiteLink">
                <p> - Link: <span><a :href="project.websiteLink" target="_blank">[Website]</a></span></p>
            </div>
            <p> - Technologies: <span class="color-green">{{ project.tags.join(", ") }}</span></p>
        </div>
    </div>
</template>
  

<script>
export default {
    name: "Projects",
    data() {
        return {
            projects: [
                {
                    projectName: "DATA SCIENCE: PREDICTION OF HEART DISEASE USING AI/ML",
                    projectDescription:
                        "https://github.com/pj323/AI-ML-Project",
                    githubLink: "https://github.com/praneethravuri/prav-terminal",
                    websiteLink: "https://preejohn.dev/",
                    tags: ["Jupyter, python"],
                },
                {
                    projectName: "BIG DATA: LARGE SCALE DATA STRUCTURE PROJECTS IN GENOMIC DATA",
                    projectDescription: "Led team of two to design and develop different combinations of algorithms using C++. Employed advanced search algorithms, including Smith-Waterman, BLAST, Trie, and Trees, to identify key genetic patterns and mutations relevant to COVID-19.",
                    githubLink: "https://github.com/praneethravuri/Task-Tracker",
                    tags: ["Linux, C++"],
                },
                {
                    projectName: "STUDENT PLACEMENT DATABASE MANAGEMENT SYSTEM",
                    projectDescription: "Successfully integrated Java JDBC (Java Database Connectivity) to establish seamless communication between the frontend and the JDBMS, enabling real-time data synchronization and efficient database operations.",
                }

            ],
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/_variables.scss";

.projects {

    width: 75%;

    & div div {
        margin: 0;
    }

    & .sub-project {
        border-bottom: 2px dashed $grey;
        padding-bottom: 10px;
        margin-bottom: 30px;
    }
}

.main-content-heading{
    color: $content-heading-color;
}

a{
    color: $green;
}
</style>