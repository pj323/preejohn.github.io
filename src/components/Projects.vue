<template>
    <div class="projects">
      <div class="sub-project m-30" v-for="project in projects" :key="project.projectName">
        <p class="main-content-heading">{{ project.projectName }}</p>
        <p> - {{ project.projectDescription }}</p>
  
        <div v-if="project.githubLink && project.websiteLink">
          <p> - Links: 
            <span> 
              <a :href="project.githubLink" target="_blank">[GitHub]</a> | 
              <a :href="project.websiteLink" target="_blank">[Website]</a>
            </span>
          </p>
        </div>
  
        <div v-else-if="project.githubLink">
          <p> - Link: 
            <span><a :href="project.githubLink" target="_blank">[GitHub]</a></span>
          </p>
        </div>
  
        <div v-else-if="project.websiteLink">
          <p> - Link: 
            <span><a :href="project.websiteLink" target="_blank">[Website]</a></span>
          </p>
        </div>
  
        <p v-if="project.tags && project.tags.length > 0"> 
          - Technologies: 
          <span class="color-green">{{ project.tags.join(", ") }}</span>
        </p>
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
            projectDescription: "Developed a machine learning model to predict heart disease.",
            githubLink: "https://github.com/praneethravuri/prav-terminal",
            websiteLink: "https://preejohn.dev/",
            tags: ["Jupyter", "Python", "Machine Learning"],
          },
          {
            projectName: "BIG DATA: LARGE SCALE DATA STRUCTURE PROJECTS IN GENOMIC DATA",
            projectDescription: "Led a team to develop algorithms using C++, focusing on key genetic patterns relevant to COVID-19.",
            githubLink: "https://github.com/praneethravuri/Task-Tracker",
            tags: ["Linux", "C++", "Genomic Data"],
          },
          {
            projectName: "STUDENT PLACEMENT DATABASE MANAGEMENT SYSTEM",
            projectDescription: "Integrated Java JDBC for seamless communication between frontend and database.",
            tags: ["Java", "JDBC", "Database"],
          }
        ],
      };
    },
  };
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
  
  .main-content-heading {
    color: $content-heading-color;
  }
  
  a {
    color: $green;
  }
  </style>
  