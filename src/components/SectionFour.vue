<template>
    <div id="section-four">
        <div class="container d-flex flex-column align-items-center">
            <h1 class="primary-font">Our Shop</h1>
            <div class="icons d-flex my-5">
                <div class="icon text-center me-5">
                    <i class="fs-1 fas fa-globe"></i>
                    <h4>spedizioni ovunque nel mondo</h4>
                </div>
                <div class="icon text-center">
                    <i class="fs-1 far fa-credit-card"></i>
                    <h4>qualsiasi carta di credito</h4>
                </div>
            </div>
            <p class="fs-2">puoi trovare tutti i nostri prodotti nel <a href="https://www.etsy.com/it/shop/vasamenapoli" target="_blank">nostro shop Etsy</a>!</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SectionFour'
}
</script>

<style scoped lang="scss">
@import '../style/utilities.scss';
    #section-four{
        padding: 150px 0;
    }
</style>