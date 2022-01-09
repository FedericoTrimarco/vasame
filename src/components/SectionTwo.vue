<template>
    <div id="section-two">
        <div class="container text-center">
            <h1 class="mb-5 primary-font fs-80px">About</h1>
            <div class="row pt-5 mb-5 align-items-center">
                <div class="col-6 d-lg-block d-none">
                    <div id="carouselExampleFade" class="carousel slide carousel-fade" data-bs-ride="carousel">
                        <div class="carousel-inner">
                            <div class="carousel-item active" data-bs-interval="1800">
                                <img src="../assets/imma.jpeg" class="d-block w-100" alt="imma">
                            </div>
                            <div class="carousel-item" data-bs-interval="1800">
                                <img src="../assets/genni.jpeg" class="d-block w-100" alt="genni">
                            </div>
                            <div class="carousel-item" data-bs-interval="1800">
                                <img src="../assets/nunzia.jpeg" class="d-block w-100" alt="nunzia">
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6 col-md-12 px-5 text-md-center text-lg-start">
                    <h3>CHI SIAMO ?</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas harum animi vero et rem consectetur odio. Delectus maiores modi voluptas et ea a, pariatur, totam, porro aspernatur labore voluptate beatae. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Cumque ipsam, voluptatem deserunt, sint, quaerat dolore recusandae at sit.</p>
                    
                    <img src="../assets/stripe.png" alt="stripe" class="w-25 mb-4">
                    
                    <h3>COM'E` NATO IL PROGETTO ?</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas harum animi vero et rem consectetur odio. Delectus maiores modi voluptas et ea a, pariatur, totam, porro aspernatur labore voluptate beatae. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Cumque ipsam, voluptatem .</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SectionTwo'
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    #section-two{
        padding: 200px 0;
        border-bottom: 2px solid lightgray;

        h1{
            color: $firstColor;
        }

        h3{
            color: $firstColor;
        }

        p{
            color: gray;
            font-size: 20px;
        }
    }
    @media screen and (max-width: 991px) {
        #section-two{
            h1{
                font-size: 60px;
            }
        }
    }
</style>