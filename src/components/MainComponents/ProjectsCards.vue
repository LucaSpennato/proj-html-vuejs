<template>
    <div class="col-4 mb-4">
        <div id="card-projects">
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
        card: Object,
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
    #card-projects{
            position: relative;
            transition: transform 200ms linear;

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

            &:hover{
                transform: scale(1.1);
            }
        }
</style>