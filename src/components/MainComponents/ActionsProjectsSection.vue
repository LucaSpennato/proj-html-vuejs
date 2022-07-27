<template>
    <section id="action-projects" class="container-fluid flex-center">
        <div class="container-medium p-4">
            <div class="row text-center">
                <div class="infos">
                    <h6 class="text-uppercase">
                        we do more for everyone
                    </h6>
                    <h1 class="fw-bold py-4">
                        actions &
                        <span>projects</span>
                    </h1>
                </div>
            </div>
        </div>
    </section>

</template>

<script>
export default {
    name: 'ActionsAndProjects',
    data: function(){
        return{
            
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

    #action-projects{
        margin-top: 6rem;
        .infos{
                h1{
                    text-transform: capitalize;
                }
                span{
                    @include companyStyledWord;
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