<template>
    <section id="contact" class="contact-section">
        <v-container>
            <v-row>
                <v-col>
                    <h1 class="text-center">Contact Information</h1>
                </v-col>
            </v-row>
            <v-row>
                <v-col sm="5" offset-sm="3" class="d-flex justify-space-around">
                    <v-icon></v-icon>
                    <a href="https://github.com/golfbauer">
                    <img 
                    class="contact-icon"
                    src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg"
                    >
                    </a>
                    <a href="https://www.linkedin.com/in/henri-truetsch-16a367222/">
                    <img 
                    class="contact-icon"
                    src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg"
                    >
                    </a>
                    <a href="mailto:henri.truetsch@gmail.com">
                    <img 
                    class="contact-icon"
                    src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/gmail.svg"
                    >
                    </a>
                    <a href=""> <!--TODO: get a fucking link for discord --> 
                    <img 
                    class="contact-icon"
                    src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/discord.svg"
                    >
                    </a>
                </v-col>
            </v-row>
        </v-container>
    </section>
</template>

<style scoped>
.contact-section {
   background-color: #FFD563; 
}

.contact-icon {
    height: 40px;
}
</style>