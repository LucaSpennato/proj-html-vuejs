<template>
  <section id="get-touch">
    <div class="container flex-center">
        <div class="row col-10">
                <div class="col-7 infos">
                    <SectionsHeadings :info="titleInfo" />
                    <div class="input-group">
                        <div class="top-input">
                            <input type="text" placeholder="Name">
                            <a href="#" @click.prevent>
                                <img id="input-name-img" 
                                :src="require('../../assets/general/input-image.png')" alt="input-name-img">
                            </a>
                            <input type="email" placeholder="Email">
                        </div>
                        <div class="middle-input">
                            <input type="tel" placeholder="Phone">
                            <select name="more-info">
                                <option selected value="">More info</option>
                                <option value="1">Option 1</option>
                                <option value="2">Option 2</option>
                                <option value="3">Option 3</option>
                            </select>
                        </div>
                        <textarea name="area-message" cols="30" rows="10" placeholder="Message"></textarea>
                </div>
                    </div>
            <div class="right-side col-5">
                <h5>
                    Example Inc.
                </h5>
                <div>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                </div>
                <div>
                    Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                </div>
                <ul class="contact p-0">
                    <li v-for="(contact, index) in contactUsInfo" :key="index">
                        <a :href="contact.url" @click.prevent>
                            <i :class="iconPath(contact)"></i>
                            <span>{{ contact.text }}</span>
                        </a>
                    </li>
                    
                </ul>
                <a class="view-map btn" href="#" @click.prevent>view map</a>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import SectionsHeadings from "./SectionsHeadings.vue";

export default {
    name: 'GetInTouch',
    components:{
        SectionsHeadings,
    },
    methods:{
        iconPath: function(object){
            return 'bi bi-' + object.icon + '-fill';  
        }
    },
    data: function(){
        return{
            titleInfo: {
                topSubtitle: "send a message",
                title: "get in touch",
                description: 'We will responde to your message as soon as possible',
                typeOne: true,
                typeTwo: false,
            },
            contactUsInfo: [
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
                    icon: 'geo-alt',
                    url: '#',
                    text: 'main avenue, 987',
                },
            ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

    #get-touch{
        padding: 7rem;

        .input-group{
            padding-top: 1.5rem;
            input, select, textarea{
                border: none;
                background-color: $McGrayNurse;
                padding: .6rem;
                margin: .3rem;
                color: gray;
            }
            input, select{
                width: calc(50% - .6rem);
            }
            textarea, div{
                width: 100%;
            }
            .top-input{
                position: relative;
            }
            #input-name-img{
                position: absolute;
                z-index: 1;
                transform: translate(-50%, -50%);
                top: 50%;
                left: 46%;
            }
        }

        .right-side{
            padding: 1rem 1.5rem;
            h5{
                font-weight: bold;
            }
            div{
                padding: .9rem 0;
                color: $secondaryTextColor;
            }
            .contact{
                margin: 2rem 0;
                list-style: none;
                li{
                    margin: 1.5rem 0;
                }
                a{
                    text-decoration: none
                }
                i{
                    @include companyStyledWord;
                    padding: .7rem;
                    border-radius: 50%;
                }
                span{
                    color: $CcBluelagoon;
                    margin-left: .5rem;
                    text-transform: capitalize;
                } 
            }

            .view-map{
                @include inactiveElementBrandColor;

                &:hover{
                @include activeElementBrandColor;
            }
        }
    }
}

</style>