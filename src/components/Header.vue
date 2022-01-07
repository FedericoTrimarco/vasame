<template>
    <header class="d-flex justify-content-between align-items-center position-fixed w-100 px-5">
        <div class="img-logo">
            <img src="../assets/logo-vasame-transparent.png" alt="logo-vasame">
        </div>

        <nav class="info">
            <ul class="list-unstyled d-flex fs-1 primary-font">
                <li>
                    <a href="#section-two">About</a>
                </li>
                <li class="mx-5">
                    <a href="#section-three">Our items</a>
                </li>
                <li>
                    <a href="#section-four">Our Shop</a>
                </li>
            </ul>
        </nav>

        <div class="img-logo">
            <img src="../assets/logo-vasame-transparent.png" alt="logo-vasame">
        </div>
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
        z-index: 6;
        img{
            height: 150px;
        }


        li{
            a{
                color: $thirdPurple;
                text-decoration: none;
            }
    
            &::after{
                content: '';
                display: block;
                height: 5px;
                width: 0;
                margin: 0 auto;
                background-color: $thirdPurple;
                transition: width .3s linear;
                border-radius: 15px;
            }

            &:hover::after{
                    width: 100%;
            }
        }
    }
</style>