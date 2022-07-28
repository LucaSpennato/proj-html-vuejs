<template>
  <div class="col-12 infos">
        <h6 class="text-uppercase">
            {{ info.topSubtitle }}
        </h6>
        <h1 class="fw-bold py-4">
            {{ info.title }}
            <span>
                {{ info.brandTitle }}
            </span>
        </h1>
        <p v-if="info.description">
            {{ info.description }}
        </p>
    </div>
</template>

<script>
export default {
    name: 'HeadingTypeOne',
    props:{
        info: Object,
    },
    methods:{
        log(element){
            console.log(element)
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
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

</style>