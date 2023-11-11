<template>
    <div class="generate-exp">
        <div class="work" v-for="exp in experience" :key="exp.company">
            <p class="main-content-heading">{{ exp.position }} @ {{ exp.company }}</p>
            <p>- {{ exp.dateRange }}</p>
            <p>- {{ exp.location }}</p>
            <div class="work-content" v-for="content in exp.content" :key="content" style="margin: 0;">
                <p>- {{ content }}</p>
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    name: "Experience",
    data() {
        return {
            experience: [
                {
                    company: "Amazon AWS",
                    position: "Software Development Engineer",
                    location: "Seattle, WA",
                    dateRange: "Sept. 2022 - Oct. 2023",
                    content: [
                        "Spearheaded the management of flexible data derived from IoT devices(JSON) feature, employing customers to index updates 10x times efficiently and aggregate data queries across multiple sources.",
                        "Developed and delivered a comprehensive suite of tools, powered by Elasticsearch and DynamoDB, to device owners for advanced device management and data analysis capabilities."

                    ]
                },
                {
                    company: "Village Book Builders",
                    position: "Backend Software Engineer Intern",
                    location: "Utah",
                    dateRange: "May 2021 - Aug. 2021",
                    content: [
                        "Implemented front-end performance optimizations, including lazy loading and code minification, resulting in a significant 15 % reduction in the website's overall file size",
                        "Collaborated with UX designers to ensure seamless compatibility between design elements and application programming interfaces, guaranteeing optimal product functionality"
                    ]
                },
                {
                    company: "Digisec360",
                    position: "Data Engineer",
                    location: "Bangalore, India",
                    dateRange: "Aug. 2020 - Dec. 2021",
                    content: [
                        "Orchestrated the development of a dynamic company web page, employing a versatile technology stack comprising JavaScript, PHP, HTML, CSS and Bootstrap to enhance user experience and interactivity.",
                        "Collaborated with software architects to design and implement complex features, ensuring code quality and performance using C++."
                    ]
                },
                {
                    company: "SELVITATE TECHNOLOGIES",
                    position: "Web Developer",
                    location: "Bangalore, India",
                    dateRange: "Aug. 2019 - Aug. 2020",
                    content: [
                        "Proficiently employed systems engineering methods, tools, and processes to develop Sales Engine using PHP, AngularJS, and SQL.",
                        "Collaborated with front-end developers to integrate user-facing elements, and optimized performance through PHP for Selvitate Tech's web applications."
                    ]
                }
            ]
        };
    }
};
</script>


<style scoped lang="scss">
@import "../styles/_variables.scss";
.work{
    padding-bottom: 10px;
    margin-bottom: 30px;
    border-bottom: 2px dashed $grey;
}

.main-content-heading{
    color: $content-heading-color;
}

.generate-exp{
    width: 75%;
}
</style>