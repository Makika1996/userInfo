<template>
    <v-form>
        <v-text-field
                class="email"
                v-model="user.email"
                label="E-mail"
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
    .email {
        width: 835px;
    }
</style>


