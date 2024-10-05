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
                    company: "HCLTech",
                    position: "Software Engineer",
                    location: "Chicago, IL (Remote)",
                    dateRange: "March 2023 - Present",
                    content: [
                        "Developed Java-based policy management tools for a cloud security platform using Core Java, Spring, and Hibernate, resulting in a 30% increase in deployment efficiency; managed version control with Git.",
                        "Developed and deployed microservices architecture using containerization technologies, enhancing the agility and scalability of SaaS products.",
                        "Deployed a microservices architecture handling over 500 transactions per second, improving system scalability by 150% and reducing operational costs by 30% through containerization with Docker and Kubernetes orchestration.",
                        "Engineered a robust back-end processing system that scaled to handle a threefold increase in concurrent user traffic, employing Java and using Spring Boot framework, which enhanced system reliability.",
                        "Authored comprehensive JUnit tests for 50+ classes, increasing code coverage by over 40% and ensuring robust platform functionality.",
                        "Integrated JFrog Artifactory to manage artifacts and dependencies, improving build consistency and accelerating the development cycle.",
                        "Implemented Continuous Integration/Continuous Deployment (CI/CD) using GitLab, reducing deployment time and minimizing human errors.",
                        "Utilized ElasticSearch for implementing real-time search and logging capabilities, improving data analytics and operational visibility by over 50%.",
                        "Optimized SQL queries and database schemas on PostgreSQL, resulting in a 25% improvement in data retrieval times for high-load operations."
                    ]
                },
                {
                    company: "Amazon AWS",
                    position: "Software Development Engineer",
                    location: "Seattle, WA",
                    dateRange: "September 2022 - March 2023",
                    content: [
                        "Performed various tasks, including Java 8 and Ruby on Rails, which had a significant impact on customers.",
                        "Utilized dependency injection techniques i.e. Dagger & Spring Beans to enhance smoothness & loose coupling of System.",
                        "Managed and optimized large datasets using Hive at Amazon, ensuring efficient data processing and storage.",
                        "Partnered with data scientists to restructure data accessibility for business, enhancing data-driven decision-making boosting productivity by 25%.",
                        "Implemented & maintained services by Thrift at Amazon, facilitating communication between various microservices.",
                        "Developed and delivered a comprehensive suite of tools, powered by Elasticsearch and DynamoDB, to device owners for advanced device management and data analysis capabilities.",
                        "Spearheaded the management of flexible data derived from IoT devices (JSON) feature, improving data indexing 10x times efficiently and aggregating data queries across multiple sources.",
                        "Worked on the Region Build Project, deploying services for new regions, conducting pipeline migration, synthesis, and load testing with 1M connected devices."
                    ]
                },
                {
                    company: "Village Book Builders",
                    position: "Backend Software Engineer Intern",
                    location: "Utah (Remote)",
                    dateRange: "May 2021 - August 2021",
                    content: [
                        "Designed and implemented a sophisticated online web application utilizing Python and Django framework, providing seamless mentor and student engagement platforms with interactive functionalities.",
                        "Optimized application performance and load times by implementing advanced query optimizations and using Django's caching mechanisms.",
                        "Worked with Async Message processing systems like Kafka & JMS tech to process messages & integrate across systems.",
                        "Designed and implemented data processing workflows using Apache Spark, handling large-scale data sets with RDDs and DataFrames.",
                        "Integrated Hadoop ecosystem tools to manage and process data, leveraging HDFS for storage and YARN for resource management."
                    ]
                },
                {
                    company: "Selvitate Technologies",
                    position: "Junior Software Developer",
                    location: "Bengaluru, India",
                    dateRange: "August 2019 - August 2020",
                    content: [
                        "Developed interactive dashboards using JavaScript and Business Intelligence tools to visualize sales operations data, providing insights into sales performance.",
                        "Analyzed large datasets to identify key metrics and performance indicators, presenting findings to stakeholders through detailed reports and data visualization.",
                        "Carried out business analytics on least seller data from several e-commerce platforms, arranging vendor products strategically to become best sellers and increase visibility and sales.",
                        "Researched, designed & implemented scalable apps for information identification, extraction, analysis, retrieval & indexing.",
                        "Helped & implemented features of Access Request System using Java, Spring, JSP, JavaScript, and Hibernate."
                    ]
                }
            ]
        };
    }
};
</script>


<style scoped lang="scss">
@import "../styles/_variables.scss";
.work {
    padding-bottom: 10px;
    margin-bottom: 30px;
    border-bottom: 2px dashed $grey;
}

.main-content-heading {
    color: $content-heading-color;
}

.generate-exp {
    width: 75%;
}
</style>
