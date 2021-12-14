<template>
    <div>
        <h1 id="title">kusoFORM</h1>
        <v-container class="beside">
            <div class="input">
                <v-row>
                    <v-col cols="4">
                        <v-row>
                            <v-spacer
                                v-if="namePosition % 2 == 0"
                            ></v-spacer>
                            <v-col cols="3">
                                <v-text-field
                                    placeholder="Name"
                                    solo
                                    v-model="name"
                                ></v-text-field>
                            </v-col>
                            <v-spacer
                                v-if="namePosition % 3 == 1"
                            ></v-spacer>
                        </v-row>
                    </v-col>
                </v-row>
                <v-row>
                    <v-spacer
                        v-if="emailPosition % 2 == 0"
                    ></v-spacer>
                    <v-col cols="4">
                        <v-row>
                            <v-spacer></v-spacer>
                            <v-col cols="3">
                                <v-text-field
                                    placeholder="Email"
                                    solo
                                    v-model="email"
                                ></v-text-field>
                            </v-col>
                            <v-spacer
                                v-if="emailPosition % 3 == 1"
                            ></v-spacer>
                        </v-row>
                    </v-col>
                    <v-spacer></v-spacer>
                </v-row>
                <v-row>
                    <v-spacer></v-spacer>
                    <v-col cols="4">
                        <v-row>
                            <v-spacer
                                v-if="passwordPosition % 2 == 0"
                            ></v-spacer>
                            <v-col cols="3">
                                <v-text-field
                                    placeholder="Password"
                                    solo
                                    v-model="password"
                                ></v-text-field>
                            </v-col>
                            <v-spacer
                                v-if="passwordPosition % 3 == 1"
                            ></v-spacer>
                        </v-row>
                    </v-col>
                </v-row>
            </div>
        </v-container>
        <v-container>
            <v-row>
                <v-spacer></v-spacer>
                <v-col
                    cols="3"
                >
                    <v-btn
                        color="primary"
                    >
                        send
                    </v-btn>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>
<script>
export default {
    name: 'Form',
    data: () => {
        return {
            name: 'Name',
            namePosition: 0,
            email: 'Email',
            emailPosition: 0,
            password: 'Password',
            passwordPosition: 0,
        }
    },
    methods: {
        rnd(){
            this.namePosition = Math.floor(Math.random() * (11 - 7)) + 1
            this.emailPosition = Math.floor(Math.random() * (11 - 7)) + 1
            this.passwordPosition = Math.floor(Math.random() * (11 - 7)) + 1
        }
    },
    created() {
        this.rnd()
        setInterval(() =>this.rnd(), 1000);
    },
}
</script>
<style scoped>
div {
    text-align: center;
}

#title{
    font-size: 200px;
    margin: 30px;
}

.beside {
    overflow-x: scroll;
}

.input {
    width: 3000px;
}
</style>