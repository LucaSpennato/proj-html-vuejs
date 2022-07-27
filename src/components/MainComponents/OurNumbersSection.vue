<template>
  <section id="results-section" class="container-fluid flex-center">
        <div class="container-medium">
            <div class="row text-center">
                <div class="col-12 infos">
                    <h6 class="text-uppercase">
                        what are we doing
                    </h6>
                    <h1 class="fw-bold py-4">
                        <span>results</span>
                        in Numbers
                    </h1>
                </div>

                <div class="row mt-5 justify-content-between">
                    <div class="result col-3 p-0" 
                    v-for="(result, index) in companyResults" :key="index">
                        <h2>{{ result.number }}</h2>
                        <h3>{{ result.area }}</h3>
                    </div>
                </div>

            </div>
        </div>
    </section>    
</template>

<script>
export default {
    name: 'OurNumbersSection',
    data: function(){
       return{
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
        .infos{
            h1{
                text-transform: capitalize;
                color: $CcWhite;
            }
            span{
                @include companyStyledWordBg;
            }
            h6{
                color: $CcBluelagoon;
                font-size: .8rem;
            }
            p{
                color: $CcPumice;
            }
        }

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