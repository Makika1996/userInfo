<template>
    <div>
        <h1>User Page</h1>
        <v-container class="container">
            <v-card class="general">
                <NameEdit
                        :user="user"
                        @input="onUserUpdated"
                />
                <GenderEdit
                        :user="user"
                        @input="onUserUpdated"
                />
                <AgeEdit
                        :user="user"
                        @input="onUserUpdated"
                />
                <BirthdayEdit
                        :user="user"
                        @input="onUserUpdated"
                />
                <EmailEdit
                        :user="user"
                        @input="onUserUpdated"
                />
                <TelefonEdit
                        :user="user"
                        @input="onUserUpdated"
                />
                <JobTitleEdit
                        :user="user"
                        @input="onUserUpdated"
                />
            </v-card>
            <v-card class="address">
                <AddressEdit
                        :user="user"
                        @input="onUserUpdated"
                />
            </v-card>
            <v-card class="userNotes">
                <NotesEdit
                        :user="user"
                        @input="onUserUpdated"
                />
            </v-card>
            <v-card class="details">
                <UserDetails
                        :user="user"
                />
            </v-card>
        </v-container>
    </div>
</template>

<script>
    import UserDetails from './UserDetails'
    import NameEdit from './UserEdit/NameEdit'
    import AgeEdit from './UserEdit/AgeEdit'
    import BirthdayEdit from './UserEdit/BirthdayEdit'
    import EmailEdit from './UserEdit/EmailEdit'
    import AddressEdit from './UserEdit/AddressEdit'
    import GenderEdit from './UserEdit/GenderEdit'
    import JobTitleEdit from './UserEdit/JobTitleEdit'
    import NotesEdit from './UserEdit/NotesEdit'
    import TelefonEdit from './UserEdit/TelefonEdit'

    export default {
        components: {
            NameEdit,
            AgeEdit,
            BirthdayEdit,
            EmailEdit,
            AddressEdit,
            GenderEdit,
            JobTitleEdit,
            TelefonEdit,
            NotesEdit,
            UserDetails
        },
        data: function () {
            return {
                user: {
                    firstName: 'Marija',
                    lastName: 'Marinkov',
                    age: 27,
                    birthday: '1996-08-05',
                    email: 'marijamarinkov96@gmail.com',
                    street: 'Dragise Brasovana',
                    houseNumber: 14,
                    lNameDoor: 'Marinkov',
                    postCode: 21000,
                    city: 'Novi Sad',
                    country: 'Serbia',
                    gender: 'female',
                    jobTitle: 'FrontEnd Developer',
                    phone: '0691514762',
                }
            };
        },
        methods: {
            onUserUpdated: function (user) {
                this.user = user
                // this.user.firstName = user.firstName
                // this.user.lastName = user.lastName
            }
        }
    }
</script>

<style scoped>
    h1 {
        text-align: center;
        padding: 20px 0;
    }

    .container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-areas: "general address" "general notes" "details details";
    }

    .general {
        grid-area: general;
        margin-right: 20px;
        margin-bottom: 10px;
        padding: 10px 20px;
    }

    .address {
        grid-area: address;
        margin-left: 20px;
        margin-bottom: 10px;
        padding: 10px 20px;
    }

    .userNotes {
        grid-area: notes;
        margin-left: 20px;
        margin-bottom: 10px;
        padding: 10px 20px;
    }

    .details {
        grid-area: details;
        padding: 10px 20px;
    }
</style>
