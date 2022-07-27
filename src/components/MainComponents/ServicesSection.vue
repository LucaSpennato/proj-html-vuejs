<template>
  <section id="services" class="container-fluid flex-center">
    <div class="container-medium">
        <div class="row justify-content-between">
            <div class="col-8">
                <div class="text-uppercase">
                    our business areas
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
        <div class="row row-cols-3">
            <div class="services-card col rounded p-5">
                <div class="card-body">
                    <i class="bi bi-airplane fs-1"></i>
                    <h5 class="card-title">Card title</h5>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                </div>
            </div>
        </div>    
    </div>
  </section>
</template>

<script>
export default {
    name: 'ServicesSection',
    data: function(){
        return{
            servicesInfos:[
                {
                    icon: 'network',
                    title: 'audit & assurance',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'briefcase',
                    title: 'financial advisory',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'bar-chart',
                    title: 'analitics and m&a',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'airplane',
                    title: 'middle marketing',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'globe',
                    title: 'legal consulting',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
                {
                    icon: 'inbox',
                    title: 'regulatory risk',
                    text: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.',
                    url: '#',
                },
            ]
            
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #services{
        background-color: $ServicesBg;
        padding: 8rem 0;

        .services-card{
            width: 20rem;
            margin: .8rem;
            background-color: $CcWhite;
        }
    }

</style>