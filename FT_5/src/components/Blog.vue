<script setup>
    import Article from './Article.vue'

    import { ref } from 'vue'
const articles = ref ([
 { id: 1, title: 'My journey with Vue', body: 'lorem ipsum dlsd fusa jfsak iidkal asfosa dlsd fusa jfsak iidkal asfosa' },
 { id: 2, title: 'Blogging with Vue', body: 'lorem ipsum dlsd fusa jfsak iidkal asfosa dlsd fusa jfsak iidkal asfosa'},
 { id: 3, title: 'Why Vue is so fun', body: 'lorem ipsum dlsd fusa jfsak iidkal asfosa dlsd fusa jfsak iidkal asfosa'}])

 const postFontSize = ref(1)

</script>
<template>

    
    <div :style="{ fontSize: postFontSize + 'em' }">
    <Article v-for="article in articles" 
    :key="article.id" 
    :title="article.id + ' ' +article.title" 
    :body="'Text ' + article.body">
 </Article></div>
</template>