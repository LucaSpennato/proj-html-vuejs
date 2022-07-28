<template>
  <div class="infos p-0">
        <h6 class="text-uppercase">
            {{ info.topSubtitle }}
        </h6>
        <h1 class="fw-bold py-4" v-if="info.typeOne">
            {{ info.title }}
            <span class="company-styled-word">
                {{ info.brandTitle }}
            </span>
        </h1>
        <h1 v-if="info.typeTwo" class="text-light fw-bold py-4">
            <span class="company-styled-word-bg me-2">
                {{ info.brandTitle }}
            </span>
            {{ info.title }}
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

<style lang="scss" scoped>
    @import '../../scss/style.scss';
        .infos{
            h1{
                text-transform: capitalize;
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