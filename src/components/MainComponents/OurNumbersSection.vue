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
            </div>
        </div>
    </section>    
</template>

<script>
export default {
    name: 'OurNumbersSection',
    data: function(){
        
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
    }

</style>