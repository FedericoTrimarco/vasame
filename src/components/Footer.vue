<template>
    <footer class="py-5">
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <h4>info</h4>
                    <ul class="list-unstyled">
                        <li>info 1</li>
                        <li>info 2</li>
                        <li>info 3</li>
                        <li>info 4</li>
                        <li>info 5</li>
                        <li>info ...</li>
                    </ul>
                </div>
                <div class="col-4 text-center">
                    <h4>info</h4>
                    <ul class="list-unstyled">
                        <li>info 1</li>
                        <li>info 2</li>
                        <li>info 3</li>
                        <li>info 4</li>
                        <li>info 5</li>
                        <li>info ...</li>
                    </ul>
                </div>
                <div class="col-4 text-end">
                    <img src="../assets/logo-vasame-transparent.png" alt="" class="w-50">
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
    footer{
        background-color: $thirdPurple;
    }
</style>