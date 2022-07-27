<template>
    <section id="headTopSection">
        <div class="container-fluid flex-center p-3">
            <div class="row container-medium flex-between">
                <div class="col-12">
                    <ul class="list-reset">
                       <li v-for="(info, index) in  companySocialInfo" :key="index">
                            <a  @click.prevent 
                                :href="info.url">
                                <i :class="iconPath(info, index)"></i>
                                {{ info.text }}</a>
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
    methods:{
        iconPath: function(object, index){

            if(index < 3){
                return 'bi bi-' + object.icon + '-fill';
            }else{
                return 'bi bi-' + object.icon;
            }
        }
    },
    data: function(){
        return{
           companySocialInfo:[
            {
                icon: 'clock',
                url: '#',
                text: 'open hours: mon - sat - 9:00 - 18:00',
            },
            {
                icon: 'telephone',
                url: '#',
                text: '+1(305) 1234-5678',
            },
            {
                icon: 'envelope',
                url: '#',
                text: 'hello@example.com',
            },
            {
                icon: 'facebook',
                url: '#',
                text: '',
            },
            {
                icon: 'twitter',
                url: '#',
                text: '',
            },
            {
                icon: 'linkedin',
                url: '#',
                text: '',
            },
           ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    @import '~bootstrap-icons/font/bootstrap-icons.css';

    #headTopSection{
        background-color: $TopHeaderBg;
        color: $CcPumice;

        ul{
            display: flex;
            justify-content: flex-start;;

            li{
                padding: 0 .6rem;
                font-size: .9rem;
            }

            li:first-child{
                flex-grow: 1;
                text-transform: capitalize;
            }
            li a{
                color: $CcPumice;
            }
        };
    };

</style>