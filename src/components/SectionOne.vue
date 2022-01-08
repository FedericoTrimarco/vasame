<template>
    <div class="section-one">
        <div class="title w-100 h-100 d-flex justify-content-center align-items-center">
            <h1 class="primary-font">Vasame</h1>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SectionOne'
}
</script>

<style scoped lang="scss">
@import '../style/utilities.scss';
@import '../style/variables.scss';
    .section-one{
        height: 100vh;
        background-image: url('../assets/IMG_2282 (3).png');
        background-size: cover;
        background-position: bottom;

        .title{
            color: $secondColor;
            background-color: rgba(0,0,0,0.5);

            h1{
                font-size: 300px;
            }
        }
    }

</style>