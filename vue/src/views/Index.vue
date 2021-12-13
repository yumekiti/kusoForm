<template>
    <div>
        <h1 id="title">kusoFORM</h1>
        <p>
            フォーム送信できたらゲームクリアです。<br>
            短時間で送信ができるよう頑張ってください。
        </p>
        <v-btn
            class="no-btn"
            elevation="2"
            outlined
            height="100"
            rounded
        >
            <div>
                <span class="no-next">次のページへ</span><br>
                <span class="no">行かない</span>
            </div>
        </v-btn>
        <p class="next">Please <u>click</u> <span @click="next()">HERE</span> to GO to the <span style="color: #0000A5;">next page</span></p>
    </div>
</template>
<script>
export default {
    name: 'Index',
    methods: {
        next(){
            this.$router.push('/form')
        }
    },
}
</script>
<style scoped>

div{
    text-align: center;
}

#title{
    font-size: 200px;
    margin: 30px;
}

.no-btn{
    margin: 30px;
}

.no-next{
    font-size: 40px;
}

.no{
    font-size: 1px;
    color: #ddd;
}

.next{
    color: #aaa;
    position: absolute;
    bottom: 0%;
    left: 50%;
    transform: translateX(-50%);
    -webkit-transform: translateX(-50%);
    -ms-transform: translateX(-50%);
}

</style>