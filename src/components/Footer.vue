<template>
    <footer class="py-5">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-md-6 col-12 d-flex flex-column align-items-center">
                    <div>
                        <h2 class="mb-5 primary-font">info</h2>
                        <ul class="list-unstyled">
                            <li>
                                social: <a href="https://www.instagram.com/vasame.napoli/" target="_blank"><i class="fab fa-instagram insta"></i></a>
                            </li>
                            <li class="my-3">number: <a href="tel:+447927975669″">+44 7927975669</a></li>
                            <li>
                                email: <a href=" mailto: trimarcofabrizia@gmail.com" target="_blank">trimarcofabrizia@gmail.com</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-md-6 col-12">
                    <img src="../assets/logo-vasame-transparent.png" alt="" class="w-100">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    footer{
        background-color: $thirdPurple;
        li{
            font-size: 25px;
            a{
                color: $firstColor;
                text-decoration: none;
                .insta{
                    font-size: 50px;
                }

                &:hover{
                    color: $secondColor;
                }
            }
        }
    }
    /**********
    RESPONSIVE
    **********/
    @media screen and (max-width: 991px) {
        h2{
            font-size: 40px;
        }
    }
    @media screen and (max-width: 767px) {
        h2{
            text-align: center;
        }
    }
    
</style>