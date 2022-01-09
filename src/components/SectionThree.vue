<template>
    <div id="section-three">
        <div class="container text-center">
            <h1 class="my-5 pb-5 primary-font fs-80px">Gallery</h1>
            <div class="row">

                <div
                    v-for="(vase, id) in mainArray" :key="id"
                    class="vases col-lg-4 col-md-6 col-12 mb-4" @mouseleave="removeInfo"
                >
                    <div class="vase position-relative">
                        <img :src="require(`../assets${vase.imgSrc}`)" :alt="vase.title" class="w-100">
                        <div class="info position-absolute bottom-0 w-100 px-5" @click="showInfo" :class="{active : active == true}">
                            <i class="fas fa-angle-up cursor-pointer arrow" @click="showInfo"></i>
                            <h5 class="fw-normal mb-3">DISCOVER THE VASE</h5>
                            <h2 class="primary-font">{{ vase.title }}</h2>
                            <p>{{ vase.info }}</p>
                        </div>
                    </div>
                </div>

            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: 'SectionThree',
    props: {
        mainArray: Array,
    },
    data(){
        return{
            active: false,
            opacity: false,
        }
    },
    methods:{
        showInfo(){
            this.active = !this.active;
        },
        removeInfo(){
            this.active = false;
        },
        removeOpacity(){
            this.opacity = !this.opacity;
        },
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    #section-three{
        background-color: $thirdPurple;
        padding: 180px 0;
        border-bottom: 1px solid lightgray;
        h1{
            color: $firstColor;
        }
        .vases{
            .vase{
                border-radius: 10px;
                overflow: hidden;
                transition: transform .5s linear;
            }
        }
    }
    /**********
    RESPONSIVE 
    ***********/
    @media screen and (min-width: 991px) {
        .vases{
            .vase{
                .info{
                    height: 0;
                    background: rgba(255, 255, 255, 0.616);
                    opacity: 0;
                    transition: all .5s linear;
                }
                &:hover {
                    transform: scale(1.5);
                    z-index: 5;
                    .info{
                        opacity: 1;
                        height: 70px;
                        transition: height .5s;
                        &.active{
                            height: 100%;
                            i{
                                transform: rotate(180deg);
                            }
                        }
                    }
                }
            }
        }
    }
    @media screen and (max-width: 991px) {
        .arrow, h5{
            display: none
        }
        .vases{
            .vase{
                .info{
                    height: 100%;
                    background: rgba(255, 255, 255, 0.616);
                    opacity: 0;
                    transition: opacity .5s linear;
                }
                &:hover {
                    .info.active{
                        opacity: 1;
                    }
                }
            }
        }
    }
</style>