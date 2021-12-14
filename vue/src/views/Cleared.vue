<template>
    <div>
        <h1 id="title">Successful</h1>
        <v-btn
            style="font-size: 100px"
            height=300
            width=600
            @click="this.back"
        >もう一度</v-btn>

        <div class="data"
            v-if="this.$route.params.name"
        >
            <h2>フォームデータ</h2>
            <p>
                name : 
                <span v-text="this.$route.params.name.toString()"></span>
            </p>
            <p>
                email : 
                <span v-text="this.$route.params.email.toString()"></span>
            </p>
            <p>
                password : 
                <span v-text="this.$route.params.password.toString()"></span>
            </p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Cleared',
    methods: {
        back(){
            this.$router.push('/')
        }
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

.data {
    margin-top: 80px;
}
</style>