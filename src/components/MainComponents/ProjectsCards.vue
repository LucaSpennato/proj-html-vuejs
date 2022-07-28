<template>
  <div class="col-12">
            <div class="card-projects"
                v-for="(card, index) in projectsInfos" :key="index">
            <img class="img-fluid rounded" 
                :src="imgPath(card)" 
                :alt="imgPath(card) + 'project image'">
            <p class="rounded">{{ card.text }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProjectsCards',
    props:{
        projectsInfos: Array,
    },
    methods:{
        imgPath: function(object){
            return require('../../assets/projects/project-' + object.img + '.jpg');
        }
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';
    .card-projects{
            display: inline-block;
            width: calc((100% / 3) - 1.6rem);
            margin: .8rem;
            position: relative;

            p{
                position: absolute;
                width: 100%;
                height: 100%;
                display: flex;
                align-items: flex-end;
                padding: 2rem 1rem;
                font-weight: bold;
                font-size: 1.2rem;
                color: $CcWhite;
                background-color: rgba(black, .4);
                top: 0;
            }
        }
</style>