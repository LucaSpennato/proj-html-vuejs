<template>
  <div class="infos p-0">
        <h6 class="text-uppercase">
            {{ info.topSubtitle }}
        </h6>
        <h1 class="fw-bold py-4" v-if="info.typeOne">
            {{ splitFirstTitleWord(info.title) }}
            <span class="company-styled-word">
                {{ splitLastTitleWord(info.title) }}
            </span>
        </h1>
        <h1 v-if="info.typeTwo" class="text-light fw-bold py-4">
            <span class="company-styled-word-bg me-2">
                {{ splitFirstTitleWord(info.title) }}
            </span>
            {{ splitLastTitleWord(info.title) }}
        </h1>
        <p v-if="info.description">
            {{ info.description }}
        </p>
    </div>
</template>

<script>
export default {
    name: 'SectionHeadings',
    props:{
        info: Object,
    },
    methods:{
        splitLastTitleWord(string){
        let word = string.split(" ");
        if(word.length === 3 && this.info.typeTwo === true){
            let words = word[word.length - 2] + ' ' + word[word.length - 1];
            return words;
        }else{
            return word[word.length - 1];
        }
      },
        splitFirstTitleWord(string){
        let word = string.split(" ");
        if(word.length === 3 && this.info.typeOne === true){
            let words = word[0] + ' ' + word[1];
            return words;
        }else{
            return word[0];
        }
      },
    }
}
</script>

<style lang="scss" scoped>
    @import '../../scss/style.scss';
        .infos{
            h1{
                text-transform: capitalize;
                font-weight: 900;
            }
            h6{
                color: $brandTextColor;
                font-size: .8rem;
            }
            p{
                color: $secondaryTextColor;
                font-size: .8rem;
            }
        }

</style>