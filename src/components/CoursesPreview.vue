<template>
    <div>
        <div class="container">
            <div class="row my_width">
                <div class="col-8">
                    <img  src="../assets/img/cat_1-770x375.jpg" alt="Software Development">
                    <div class="d-flex justify-content-between">
                        <span>Software Development</span>
                        <span>5 Courses</span>
                    </div>
                </div>
                <div class="col-4">
                    <img  src="../assets/img/cat_2-740x310.jpg" alt="Art">
                    <div class="d-flex justify-content-between">
                        <span class="mb-3">Art</span>
                        <span>8 Courses</span>
                    </div>
                    <img  src="../assets/img/cat_3-740x310.jpg" alt="Material Design">
                    <div class="d-flex justify-content-between">
                        <span class="mb-2">Material Design</span>
                        <span>5 Courses</span>
                    </div>
                </div>
                <div class="col-4">
                    <img  src="../assets/img/cat_5-740x310.jpg" alt="Music">
                    <div class="d-flex justify-content-between">
                        <span class="mb-2">Music</span>
                        <span>5 Courses</span>
                    </div>
                </div>
                 <div class="col-4">
                    <img  src="../assets/img/cat_4-740x310.jpg" alt="Exercise">
                    <div class="d-flex justify-content-between">
                        <span class="mb-2">Exercise</span>
                        <span>7 Courses</span>
                    </div>
                </div>
                 <div class="col-4">
                    <img  src="../assets/img/cat_6-740x310.jpg" alt="Photography">
                    <div class="d-flex justify-content-between">
                        <span class="mb-2">Photography</span>
                        <span>4 Courses</span>
                    </div>
                </div>
               
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CoursesPreview',

}
</script>

<style lang="scss" scoped>
    img{
        width: 100%;
        object-fit: cover;
        object-position: center;
        margin-bottom: 10px;
    }
</style>