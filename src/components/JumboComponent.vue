<template>
    <div class="jumbo">
        <button><a href="#nogo">current series</a> </button>
    </div>
</template>

<script>
export default {
    name: 'JumboComponent'
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.jumbo {
    background-image: url('../../public/img/jumbotron.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 40vh;
    position: relative;
}

button {
    position: absolute;
    bottom: -20px;
    left: 210px;
    background-color: $lightblue ;
    height: 40px;
    padding: 10px;
    border: none;
    color: white;
    margin-top: 10px;
    ;

    a {
        text-transform: uppercase;
        color: $lightwhite;
        font-size: 1.2em;
        text-decoration: none;
        font-weight: bold;
    }
}
</style>