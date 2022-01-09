<template>
    <div class="section-one">
        <div class="title w-100 h-100 d-flex justify-content-center align-items-center position-relative">
            <video width="100%" height="100%" autoplay muted loop>
                <source src="../assets/video.mp4" type="video/mp4">
            </video>
            <h1 class="position-absolute top-50 start-50 translate-middle primary-font">Vasame</h1>
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
        video{
            object-fit: cover;
        }
        .title{
            color: $secondColor;

            h1{
                font-size: 200px;
                color: rgba(114, 134, 70, 0.781);
            }
        }
    }

</style>