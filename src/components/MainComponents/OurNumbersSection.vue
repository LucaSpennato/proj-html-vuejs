<template>
  <section id="results-section" class="container-fluid">
    <div class="container flex-center">
        <div class="container-medium">
            <div class="row text-center">

                <SectionsHeadings :info="titleInfo" />
                
                <div class="row mt-5 justify-content-between">
                    <div class="result col-3 p-0" 
                    v-for="(result, index) in companyResults" :key="index">
                        <h2>{{ result.number }}</h2>
                        <h3>{{ result.area }}</h3>
                    </div>
                </div>

            </div>
        </div>
    </div>
    </section>    
</template>

<script>
import SectionsHeadings from "./SectionsHeadings.vue";

export default {
    name: 'OurNumbersSection',
    components:{
        SectionsHeadings,
    },
    data: function(){
       return{
            titleInfo: {
                topSubtitle: "what are we doing",
                title: "in numbers",
                brandTitle: "results",
                description: false,
                typeOne: false,
                typeTwo: true,
            },
        companyResults:[
            {
                number: '128',
                area: 'certifications',
            },
            {
                number: '230',
                area: 'employees',
            },
            {
                number: '517',
                area: 'customers',
            },
            {
                number: '94',
                area: 'countries served',
            },
        ],
       }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    #results-section{
        background-image: url('../../assets/backgrounds/bg-7.jpg');
        padding: 6rem 0;
        .result{
            h2{
                color: $CcFountainBlue;
            }
            h3{
                text-transform: capitalize;
                color: $CcWhite;
            }
        }
    }

</style>