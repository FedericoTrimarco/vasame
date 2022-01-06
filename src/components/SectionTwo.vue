<template>
    <div id="section-two">
        <div class="container text-center">
            <h1 class="mb-5 primary-font">About</h1>
            <div class="row pt-5 align-items-center">
                <div class="col-6">
                    <div id="carouselExampleFade" class="carousel slide carousel-fade" data-bs-ride="carousel">
                        <div class="carousel-inner">
                            <div class="carousel-item active" data-bs-interval="3000">
                                <img src="../assets/imma.jpeg" class="d-block w-100" alt="...">
                            </div>
                            <div class="carousel-item" data-bs-interval="3000">
                                <img src="../assets/genni.jpeg" class="d-block w-100" alt="...">
                            </div>
                            <div class="carousel-item" data-bs-interval="3000">
                                <img src="../assets/nunzia.jpeg" class="d-block w-100" alt="...">
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 px-3 text-start">
                    <p class="fs-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas harum animi vero et rem consectetur odio. Delectus maiores modi voluptas et ea a, pariatur, totam, porro aspernatur labore voluptate beatae. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Cumque ipsam, voluptatem deserunt, sint, quaerat dolore recusandae at sit nostrum quidem quos. Tempore nihil corporis reprehenderit iste accusamus culpa? Impedit, delectus.</p>
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
    }
</style>