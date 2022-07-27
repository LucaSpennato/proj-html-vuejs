<template>
  <section id="about-company" class="container-fluid p-0">
        <div class="row col-12 m-0">
            <div class="col-6 d-flex justify-content-end mt-5 p-5">
                <div class="w-50">
                    <h6 class="text-uppercase">
                        about the network
                    </h6>
                    <h1 class="fw-bold py-4">
                        <span class="company-styled-word">The</span>
                        Company
                    </h1>
                    <p>
                        We are leaders in providing consultancy with a set of cutting-edge technologies and a team of experienced and renowed professionals. These are some options that you can hire.
                    </p>
                </div>
            </div>
            <div class="col-6 p-0">
                <img class="w-100" :src="require('../../assets/backgrounds/about-4.jpg')" alt="about-image">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AboutTheCompany',
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #about-comapny{   
        h6{
            color: $CcBluelagoon;
        }
        p{
            color: gray;
        }
    }
</style>