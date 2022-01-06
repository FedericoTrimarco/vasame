<template>
    <header class="d-flex justify-content-around align-items-center position-fixed w-100">
        <div class="img-logo">
            <img src="../assets/logo-vasame-transparent.png" alt="logo-vasame">
        </div>

        <nav class="info">
            <ul class="list-unstyled d-flex fs-3 ">
                <li>
                    <a href="#section-two">about</a>
                </li>
                <li class="mx-5">
                    <a href="#section-three">our items</a>
                </li>
                <li>
                    <a href="#section-four">shop</a>
                </li>
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
@import '../style/utilities.scss';
    header{
        background-color: $thirdColor;
        z-index: 1;
        img{
            height: 150px;
        }
    }
</style>