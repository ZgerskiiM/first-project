<script setup>
import { ref } from "vue"

const dialog = ref(false)


const users = ref([
    {name:""},
])

</script>

<template>
    <v-btn
    @click="dialog =! dialog"
    class = mb-5>
        Start
    </v-btn>

    <v-card
        v-if = "dialog"
        class = "d-flex flex-column align-center justify-center"
        width =500px
        height=600px
        border-radius=40px
        background-color=white>
        <h2>Add person</h2>
        <v-form v-model="valid">
            <v-container>
                <v-text-field
                    v-model="firstname"
                    :rules="nameRules"
                    label="Enter Name">
                </v-text-field>
                <v-btn
                    class = "mt-5" 
                    @click="users.push({name:firstname}), firstname = ''">
                        Add User
                    </v-btn>
    </v-container>
    <div
     v-for="(user, i) in users" :key="i"
     >
     <v-card
     border-color = white
     color = white
     rounded
     solo
     flat
     class = "d-flex flex-column align-items-center mt-5"> {{user.name}}
            <v-btn
            @click="users.splice(i, 1)"
            append-icon="mdi-close">
            </v-btn>
    </v-card>

    </div>
    </v-form>
        <v-btn
        @click="dialog = false"
        class = mt-5>
            Close
        </v-btn>
        <v-btn
        class = mt-5>
            Continue
        </v-btn>
    </v-card>
</template>

<style scoped>

</style>