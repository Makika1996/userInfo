<template>
    <v-row>
        <p>Sex:</p>
        <v-btn>
            Female
        </v-btn>
        <v-btn>
            Male
        </v-btn>
        <v-btn>
            Other
        </v-btn>
    </v-row>
</template>

<script>
    export default {
        components: {},
        props: [
            'user'
        ],
        watch: {
            female (val) {
                this.female = !val
            },
            male (val) {
                this.male = !val
            },
            other (val) {
                this.other = !val
            },
        },
    }
</script>

<style scoped>
    p {
        margin: 0 10px;
    }

    .female, .male, .other {
        align-items: center;
        margin: 0 10px;
    }
</style>