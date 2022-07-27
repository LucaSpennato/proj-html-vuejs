<template>
  <section id="services" class="container-fluid flex-center">
    <div class="container-medium">
        <div class="row justify-content-between">
            <div class="col-8">
                <div class="text-uppercase">
                    our business area
                </div>
                <h1 class="fw-bold">
                    Exellence in <span class="company-styled-word">Services</span>
                </h1>
                <p>
                    We are leaders in providing consultancy with a set of cutting-edge technologies and a team of experienced and renowed professionals. These are some options that you can hire.
                </p>
            </div>
            <div class="col-2 d-flex align-items-end justify-content-end">
                <a class="text-uppercase btn activeGreenLink px-4" @click.prevent href="#">see all</a>
            </div>
        </div>
        <div class="row">
            
        </div>    
    </div>
  </section>
</template>

<script>
export default {
    name: 'ServicesSection',
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #services{
        background-color: $ServicesBg;
    }

</style>