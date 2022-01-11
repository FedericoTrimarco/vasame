<template>
    <header class="position-fixed w-100 px-lg-5 pe-5">
        <div class="d-flex justify-content-between align-items-center">
            <div class="img-logo">
                <img src="../assets/logo-vasame-transparent.png" alt="logo-vasame">
            </div>
            <!-- navbar -->
            <nav class="info d-none d-lg-block">
                <ul class="list-unstyled d-flex fs-1 primary-font">
                    <li
                        class="me-5"
                        v-for="(el, id) in mainArray" :key="`link-${id}`"
                    >
                        <a :href="el.directory">{{ el.title }}</a>
                    </li>
                </ul>
            </nav>
            <!-- second-logo -->
            <div class="img-logo d-none d-lg-block">
                <img src="../assets/logo-vasame-transparent.png" alt="logo-vasame">
            </div>

            <i class="hamburger fas fa-bars fs-1 d-lg-none" @click="showRemoveInfo"></i>

        </div>


        <div class="responsive-info text-center d-lg-none" :class="{active : active == true}">
            <ul class="list-unstyled pt-4 primary-font border h-100">
                <li
                    @click="showRemoveInfo"
                    v-for="(el, id) in mainArray" :key="`link-${id}`"
                >
                    <a :href="el.directory">{{ el.title }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name:'Header',
    props: {
        mainArray: Array,
    },
    data() {
        return{
            active: false,
        }
    },
    methods: {
        showRemoveInfo() {
            this.active = !this.active;
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';
@import '../style/utilities.scss';
    header{
        background: rgb(255,220,254);
        background: linear-gradient(
            180deg, rgba(255,220,254,0.8603816526610644) 52%,
            rgba(255,220,254,0.7203256302521008) 88%
        );
        z-index: 2;
        border: 1px solid $fourth;
        img{
            height: 100px;
        }

        li{
            a{
                color: $firstColor;
                text-decoration: none;
            }
    
            &.me-5::after{
                content: '';
                display: block;
                height: 5px;
                width: 0;
                margin: 0 auto;
                background-color: $secondColor;
                transition: width .3s linear;
                border-radius: 15px;
            }

            &:hover::after{
                    width: 100%;
            }
        }
    }

    .responsive-info{
        height: 0;
        transition: height .2s linear;
        overflow: hidden;
        background-color: $bgTrasnparent;
        width: 100vw;
        font-size: 3rem;
        &.active{
            height: 100vh;
        }
    }
    @media screen and (max-width: 991px) {
        header{
            img{
                height: 80px;
            }

        }
    }
</style>