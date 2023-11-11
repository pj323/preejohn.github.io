<template>
    <div v-for="skill in skills" :key="skill.skillType">
        <p><span class="main-content-heading">{{ skill.skillType }}:</span> <span>{{ skill.skillsList.join(", ") }}</span></p>
        <br>
    </div>
</template>

<script>
export default {
    name: "Skills",
    data() {
        return {
            skills: [
                { skillType: "Languages", skillsList: ["C, C++, Python, R, SQL, Java, React, PHP, Bash, .NET, Angular, jQuery and JavaScript"] },
                { skillType: "Web Technology", skillsList: ["HTML, CSS, Bootstrap, JavaScript, RxJs, PHP, Node, NPM, REST API, Cloud (AWS, GCP, Azure)"] },
                { skillType: "Databases", skillsList: ["MySQL, PostgreSQL, Oracle, SQL Server, T-SQL, MongoDB, DynamoDB"] },
                { skillType: "AWS", skillsList: ["Elastcsearch, SQS, SNS, EC2, S3, IoT, Cloudwatch, IAM roles/policies, Lambda, API Gateway"] },
                { skillType: "Miscellaneous", skillsList: ["TensorFlow, Keras, Scikit-learn, PyTorch, NumPy, Matplotlib, Pandas, NLP, BeautifulSoup"] },
                { skillType: "Other Skills", skillsList:["GIT, Jenkins, Docker, XML, Spring MVC, Spring Core, Spring Boot, J2EE, DevOps CI/CD, Linux"]}
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