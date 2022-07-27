<template>
  <div>
    <!-- {{ links.title }}
    {{ links.links }} -->
    <ul>
        <li v-for="(link, index) in links" :key="index">
            {{ link.text }}
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'footerNav',
    props:{
        links: Array,
    }
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

</style>