<template>
    <v-form>
        <v-text-field
                class="phone"
                v-model="user.phone"
                label="Phone number"
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
    .phone {
        width: 835px;
    }
</style>

