<template>
    <v-form class="userName">
        <v-text-field
                class="fName"
                v-model="user.firstName"
                label="Firstname"
                @input="$emit('input', user)"
        />
        <v-text-field
                class="lName"
                v-model="user.lastName"
                label="Lastname"
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
    .userName {
        display: flex;
        justify-content: space-between;

    }

    .fName {
        margin-right: 50px;
    }

    .lName {
        margin-left: 50px;
    }
</style>