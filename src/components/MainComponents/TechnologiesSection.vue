<template>
  <section id="technologies" class="">
        <div class="container row justify-content-center gap-5 m-auto">
            <div class="col-1" v-for="(tech, index) in technologies" :key="index">
                <img :src="imgPath(tech)" :alt="imgPath(tech) + 'th logo'">
            </div>
        </div>    
  </section>
</template>

<script>
export default {
    name: 'TechnologiesSection',
    methods:{
        imgPath: function(object){
            return require('../../assets/logos/logo-'+ object.logo + '.png');
        }
    },
    data: function(){
        return{
             technologies:[
            {
                logo: '4',
            },
            {
                logo: '5',
            },
            {
                logo: '1',
            },
            {
                logo: '2',
            },
            {
                logo: '3',
            },
            {
                logo: '4',
            },
        ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

    #technologies{
        background-color: $CcWoodsmoke;
        padding: 7rem;
        img{
            width: 6rem;
            // margin: 0 2rem;
            filter: invert(50%);
        }
    }

</style>