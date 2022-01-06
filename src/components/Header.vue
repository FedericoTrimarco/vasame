<template>
    <header class="d-flex justify-content-around align-items-center">
        <div class="img-logo">
            <img src="../assets/logo-vasame-transparent.png" alt="">
        </div>

        <nav class="info">
            <ul class="list-unstyled d-flex fs-3 ">
                <li>about</li>
                <li class="mx-4">shop</li>
                <li>our items</li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name:'Header'
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
    header{
        background-color: $firstColor;
        img{
            height: 180px;
        }
    }
</style>