<template>
    <v-form>
        <v-text-field
                class="job"
                v-model="user.jobTitle"
                label="Job Title"
                @input="$emit('input', user)"
        />
    </v-form>
</template>

<script>
    export default {
        components: {},
        props: [
            'user'
        ]
    }
</script>

<style scoped>
    .job {
        width: 835px;
    }
</style>


