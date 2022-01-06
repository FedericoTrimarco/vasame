<template>
    <div id="section-three">
        <div class="container text-center">
            <h1 class="my-5">Our Items</h1>
            <div class="row">
                <div class="col-4 mb-4">
                    <div class="vase position-relative">
                        <img src="../assets/genni.jpeg" alt="" class="w-100">
                        <div class="info position-absolute top-0 start-0 w-100 h-100 d-flex justify-content-center align-items-center">
                            <h2>LELLO</h2>
                        </div>
                    </div>
                </div>
                <div class="col-4 mb-4">
                    <div class="vase position-relative">
                        <img src="../assets/genni.jpeg" alt="" class="w-100">
                        <div class="info position-absolute top-0 start-0 w-100 h-100 d-flex justify-content-center align-items-center">
                            <h2>LELLO</h2>
                        </div>
                    </div>
                </div>
                <div class="col-4 mb-4">
                    <div class="vase position-relative">
                        <img src="../assets/genni.jpeg" alt="" class="w-100">
                        <div class="info position-absolute top-0 start-0 w-100 h-100 d-flex justify-content-center align-items-center">
                            <h2>LELLO</h2>
                        </div>
                    </div>
                </div>
                <div class="col-4 mb-4">
                    <div class="vase position-relative">
                        <img src="../assets/genni.jpeg" alt="" class="w-100">
                        <div class="info position-absolute top-0 start-0 w-100 h-100 d-flex justify-content-center align-items-center">
                            <h2>LELLO</h2>
                        </div>
                    </div>
                </div>
                <div class="col-4 mb-4">
                    <div class="vase position-relative">
                        <img src="../assets/genni.jpeg" alt="" class="w-100">
                        <div class="info position-absolute top-0 start-0 w-100 h-100 d-flex justify-content-center align-items-center">
                            <h2>LELLO</h2>
                        </div>
                    </div>
                </div>
                <div class="col-4 mb-4">
                    <div class="vase position-relative">
                        <img src="../assets/genni.jpeg" alt="" class="w-100">
                        <div class="info position-absolute top-0 start-0 w-100 h-100 d-flex justify-content-center align-items-center">
                            <h3>LELLO</h3>
                        </div>
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>

<script>
export default {
    name: 'SectionThree'
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    #section-three{
        padding: 180px 0;
        border-bottom: 1px solid lightgray;
        .col-4{
            .vase{
                border-radius: 10px;
                overflow: hidden;

                &:hover .info{
                    opacity: 1;
                }
            }
            .info{
                background: $thirdColor;
                opacity: 0;
                transition: opacity .3s linear;
            }
        }
    }

</style>