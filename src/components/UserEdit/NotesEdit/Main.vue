<template>
    <div class="notes">
        <v-textarea
                class="notes"
                v-model="user.notes"
                name="input-7-1"
                filled
                label="Your Notes"
                auto-grow
                value=""
        ></v-textarea>
    </div>
</template>

<script>
    export default {
        components: {},
        props: [
            'user'
        ],
    }
</script>

<style scoped>

</style>
