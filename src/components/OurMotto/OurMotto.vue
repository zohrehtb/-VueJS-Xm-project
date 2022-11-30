<template>
    <article 
        v-if="content" 
        class="our-motto"
    >
        <div class="our-motto__title">
            <div class="our-motto__title__content">{{content.customFields.title1}}<span>. </span></div>
            <div class="our-motto__title__content">{{content.customFields.title2}}<span>. </span></div>
            <div class="our-motto__title__content">{{content.customFields.title3}}<span>. </span></div>
        </div>
        <p class="no-margin our-motto__text" v-html="content.subtitle"/>
    </article>
</template>

<script>
export default {
    name:'ourMotto',

    props:{
        content:Object,
    }
}
</script>