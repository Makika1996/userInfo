<template>
    <table>
        <tr>
            <th class="head">Firstname:</th>
            <td class="userInfo">{{ user.firstName }}</td>
        </tr>
        <tr>
            <th class="head">Lastname:</th>
            <td class="userInfo">{{ user.lastName }}</td>
        </tr>
        <tr>
            <th class="head">Gender:</th>
            <td class="userInfo">{{ user.gender }}</td>
        </tr>
        <tr>
            <th class="head">Age:</th>
            <td class="userInfo">{{ user.age }}</td>
        </tr>
        <tr>
            <th class="head">Birthday:</th>
            <td class="userInfo">{{ formattedBirthday }}</td>
        </tr>
        <tr>
            <th class="head">Email:</th>
            <td class="userInfo">{{ user.email }}</td>
        </tr>
        <tr>
            <th class="head">Phone:</th>
            <td class="userInfo">{{ user.phone }}</td>
        </tr>
        <tr>
            <th class="head">Job Title:</th>
            <td class="userInfo">{{ user.jobTitle }}</td>
        </tr>
        <tr>
            <th class="head">Address:</th>
            <td class="userInfo">{{ user.street }}</td>
            <td class="userInfo">{{ user.houseNumber }}</td>
            <td class="userInfo">{{ user.lNameDoor }}</td>
            <td class="userInfo">{{ user.postCode }}</td>
            <td class="userInfo">{{ user.city }}</td>
            <td class="userInfo">{{ user.country }}</td>
        </tr>
        <tr>
            <th class="head">Notes:</th>
            <td class="userInfo noBorder">{{ user.notes }}</td>
        </tr>
    </table>
</template>

<script>
    import moment from 'moment'
    export default {
        components: {},
        props: [
            'user'
        ],

        computed: {
            formattedBirthday() {
                return moment(this.user.birthday).format('DD.MM.YYYY.');
            }
        }
    }
</script>

<style scoped>
    table {
    }

    .head {
        width: 100px;
        text-align: end;
    }

    .userInfo {
        border-bottom: 1px solid black;
        max-width: 300px;
        padding: 0 10px;
        overflow: auto;
    }

    .noBorder {
        border-bottom: none;
    }
</style>


