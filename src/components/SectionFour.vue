<template>
    <div id="section-four" class="position-relative">
        <div class="container d-flex flex-column align-items-center">
            <h1 class="primary-font fs-80px">Shop</h1>
            <div class="icons d-flex my-5">
                <div class="icon text-center">
                    <i class="fs-1 far fa-credit-card mb-5"></i>
                    <h4>qualsiasi carta di credito</h4>
                </div>
            </div>
            <p class="fs-2 text-center">puoi trovare tutti i nostri prodotti nel <br> <a href="https://www.etsy.com/it/shop/vasamenapoli" target="_blank">nostro shop Etsy</a>!</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SectionFour'
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    #section-four{
        padding: 150px 0;
        h1{
            color: $firstColor;
        }
        a{
            color: $firstColor;
            text-decoration: none;

            &:hover{
                color: $secondColor;
            }
        }
    }
    #section-four{
        h1{
            font-size: 60px;
        }
    }
</style>