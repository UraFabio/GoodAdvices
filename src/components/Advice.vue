<template>
    <div id="advice-container">
        <div></div>
        <p>{{ msg }}</p>
        <button class="refresh-btn" @click="getAdvice">refresh</button>
    </div>
</template>

<script>
export default {
    name: 'Advice',
    data() {
        return {
            msg:""
        }
    },
    methods:{
        async getAdvice(){

            const numeroDecimal = Math.random();
            const id = Math.floor(numeroDecimal * 224) + 1

            const req = await fetch(`https://api.adviceslip.com/advice/${id}`)

            const data = await req.json()
            this.msg = data.slip.advice
            //this.msg = data.
        }
    },
    mounted() {
        this.getAdvice()
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;500&family=Roboto:wght@100;300;500;700&display=swap');


#advice-container {
    margin: 20px;
    padding: 10px;
    background-color: rgb(164, 169, 231);
    width: 200px;
    height: 200px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 400;
    font-family: Outfit, sans-serif;
    border-radius: 100px;
}

#advice-container {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
}

#advice-container p{
    text-align: center;
}


.refresh-btn{
    background-color: #323268;
    color: #ccc;
    font-weight: bold;
    border: 1px solid #222;
    border-radius: 100px;
    padding: 5px;
    font-size: 14px;
    margin: 0 auto;
    cursor: pointer;
    transition: .5s;
}


.refresh-btn:hover{
    background-color: transparent;
    color: #222;
}
</style>