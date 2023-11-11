<template>
    <div v-for="contact in contactInfo" :key="contact.contactName">
        <p><span class="main-content-heading">[{{ contact.contactName }}]</span>: <span><a target="_blank" :href="getContactLink(contact)">{{ contact.contactLink }}</a></span></p>
    </div>
</template>

<script>
export default {
    name: "Contact",
    data() {
        return {
            contactInfo: [
                { contactName: "Github", contactLink: "https://github.com/pj323/" },
                { contactName: "LinkedIn", contactLink: "https://www.linkedin.com/in/preetham-john/" },
                { contactName: "Email", contactLink: "preethamjohn05@gmail.com" },
                { contactName: "Resume", contactLink: "https://github.com/pj323/pj323/blob/main/Preetham%20John%20Resume.pdf" },
            ],
        };
    },
    methods: {
        getContactLink(contact) {
            if (contact.contactName === "Email") {
                return "mailto:" + contact.contactLink;
            }
            return contact.contactLink;
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";

.main-content-heading{
    color: $content-heading-color;
}

</style>
