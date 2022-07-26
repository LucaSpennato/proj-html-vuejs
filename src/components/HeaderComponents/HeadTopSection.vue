<template>
    <section id="headTopSection">
        <div class="container flex-center p-2">
            <div class="row container-medium flex-between">
                <div class="col-12">
                    <ul class="list">
                        <li>
                            <i class="bi bi-clock-fill"></i> 
                            Open Hours: Mon - Sat - 9:00 - 18:00
                        </li>
                        <li>
                            ciao
                        </li>
                        <li>
                            ciao
                        </li>
                        <li>
                            ciao
                        </li>
                        <li>
                            ciao
                        </li>
                    </ul>
                    
                </div>
                
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'HeaderTopSection',
    data: function(){
        return{
           companySocialInfo:[
            {

            }
           ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/variables.scss';
    @import '../../scss/general.scss';
    @import '../../scss/containers.scss';
    @import '~bootstrap-icons/font/bootstrap-icons.css';

    #headTopSection{
        background-color: $TopHeaderBg;
        color: $CcPumice;

        ul{
            display: flex;
            justify-content: flex-start;
            list-style: none;
            padding: 0;
            margin: 0;

            li:first-child{
                flex-grow: 1;
            }
        };
    };

</style>