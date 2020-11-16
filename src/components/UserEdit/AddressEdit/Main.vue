<template>
    <v-form class="userAddress">
        <div class="streetNbr">
            <v-text-field
                    class="street"
                    v-model="user.street"
                    label="Street"
                    @input="$emit('input', user)"
            />
            <v-text-field
                    class="hNbr"
                    v-model="user.houseNumber"
                    label="House Number"
                    @input="$emit('input', user)"
            />
        </div>
        <v-text-field
                class="lNameDoor"
                v-model="user.lNameDoor"
                label="Lastname on Door"
                @input="$emit('input', user)"
        />
        <div class="cityNbr">
            <v-text-field
                    class="pCode"
                    v-model="user.postCode"
                    label="Postcode"
                    @input="$emit('input', user)"
            />
            <v-text-field
                    class="city"
                    v-model="user.city"
                    label="City"
                    @input="$emit('input', user)"
            />
        </div>
        <v-text-field
                class="country"
                v-model="user.country"
                label="Country"
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
    .streetNbr {
        display: flex;
        justify-content: space-between;
    }
    .street, .pCode {
        margin-right: 50px;
    }

    .cityNbr {
        display: flex;
        justify-content: space-between;
    }
</style>


