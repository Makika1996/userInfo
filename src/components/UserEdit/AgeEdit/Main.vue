<template>
    <v-form>
        <v-text-field
                class="age"
                v-model="user.age"
                label="Age"
                @input="$emit('input', user)"
        />
    </v-form>
</template>

<script>
    export default {
        props: [
            'user'
        ]
    }
</script>

<style scoped>
    .age {
        width: 835px;
    }
</style>