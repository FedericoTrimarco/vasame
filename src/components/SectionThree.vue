<template>
    <section id="section-three">
        <div class="container text-center">
            <h1 class="my-5 pb-5 primary-font fs-80px">Gallery</h1>
            <div class="row">

                <div
                    v-for="(vase, id) in mainArray" :key="id"
                    class="vases col-lg-4 col-6 mb-4" @mouseleave="removeInfo"
                    @click="changeSrc(id)"
                >
                    <div class="vase position-relative">
                        <img :src="require(`../assets${vase.imgSrc}`)" :alt="vase.title" class="w-100" @click="showPopup">
                        <div
                            class="info position-absolute bottom-0 w-100 px-5 cursor-pointer" 
                            :class="{active : active == true}"
                            @click="showInfo"
                        >
                            <i class="fas fa-angle-up cursor-pointer arrow" v-if="active == false"></i>
                            <i class="fas fa-chevron-down arrow" v-else></i>

                            <h5 class="fw-normal mb-3" v-if="active == false">DISCOVER THE VASE</h5>
                            <h5 class="fw-normal mb-3" v-else>HIDE THE VASE</h5>

                            <h2 class="primary-font">{{ vase.title }}</h2>
                            <p>{{ vase.info }}</p>
                            <a :href="vase.linkShop" target="_blank">SHOP NOW</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Popup for responsive vase img -->
        <div class="popup position-fixed top-0 start-0 w-100 h-100 d-lg-none d-flex justify-content-center align-items-center" :class="{active : popup == true}">
            <!-- icon for return back -->
            <i class="fas fa-times position-absolute top-0 end-0 text-white" @click="removePopup"></i>
            <!-- pupup-img -->
            <div class="w-75" @click="showInfo">
                <h4 class="text-white text-center mb-4 fs-2">Tap on the vase</h4>
                <div class="popup-img text-center position-relative">
                    <img :src="require(`../assets${mainArray[src].imgSrc}`)" alt="" class="w-100">
                    <div
                        class="info-popup position-absolute top-0 start-0 border w-100 h-100 d-flex flex-column align-items-center justify-content-center"
                        :class="{active : active == true}"
                    >
                        <div v-show="active == true" class="px-4">
                            <h4 class="text-black fs-1 primary-font">{{ mainArray[src].title }}</h4>
                            <p>{{ mainArray[src].info }}</p>
                            <a :href="mainArray[src].linkShop" target="_blank">SHOP NOW</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </section>
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
            popup: false,
            src: 0,
        }
    },
    methods:{
        showInfo(){
            this.active = !this.active;
        },
        removeInfo(){
            this.active = false;
        },
        showPopup(){
            this.popup = true;
        },
        removePopup(){
            this.popup = false;
            this.active = false;
        },
        changeSrc(id){
            this.src = id;
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    #section-three{
        background-color: $thirdPurple;
        padding: 100px 0;
        border-bottom: 1px solid lightgray;
        a{
            font-size: 25px;
            text-decoration: none;
            color: $firstColor;
            &:hover{
                color: $secondColor;
            }
        }
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
        .vase{
            .info{
                height: 0;
                background: rgba(255, 255, 255, 0.616);
                opacity: 0;
                transition: all .5s;
            }
            &:hover {
                transform: scale(1.23);
                z-index: 1;
                .info{
                    opacity: 1;
                    height: 70px;
                    .arrow{
                        animation: upAndDown 1.5s infinite ease;
                        @keyframes upAndDown{
                            0%{
                                transform: translateY(0);
                            }
                            50%{
                                transform: translateY(7px);
                            }
                            100%{
                                transform: translateY(0);
                            }
                        }
                    }
                    &.active{
                        height: 100%;
                    }
                }
            }
        }
    }
    @media screen and (max-height: 550px){
        .popup{
            padding: 0 26%;
        }
    }
    @media screen and (max-width: 991px) {
        #section-three{
            h1{
                font-size: 60px;
            }
        }
        .popup{
            background-color: rgba(0,0,0,0.5);
            opacity: 0;
            transition: opacity .5s linear;
            backdrop-filter: blur(10px);
            .popup-img{
                border-radius: 10px;
                overflow: hidden;
                img{
                    position: relative;
                }
                .info-popup{
                    background-color: rgba(255, 255, 255, 0.616);
                    opacity: 0;
                    transition: opacity .3s linear;
                    div{
                        overflow: scroll;
                    }
                    &.active{
                        opacity: 1;
                    }
                }
            }
            i{
                font-size: 50px;
                margin-top: 100px;
                margin-right: 60px;
            }
            &.active{
                opacity: 1;
                z-index: 3;
            }
        }
        .arrow, h5{
            display: none
        }
            .vases{
                z-index: 1;

            .info{
                display: none;
            }
        }
    }
</style>