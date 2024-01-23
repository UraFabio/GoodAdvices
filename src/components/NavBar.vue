<template>
    <header id="header">
        <img src="../assets/bulb.png" alt="">
        <nav>
            <a id="refreshAll" href="">Refresh All</a>
        </nav>
        <div></div>
    </header>
</template>

<script>
export default {
    name: "NavBar"
}
</script>

<style scoped>
#header {
    height: 10vh;
    background-color: #373768;
    color: #ccc;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
}
img{
    height: 60%;
}

#refreshAll {
    font-size: 22px;
}

</style>