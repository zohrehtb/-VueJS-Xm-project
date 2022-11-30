<template>
    <header class="section-title" :class="`section-title--${mode}`">
        <template  v-if="mode === '1'" >
            <h2 class="ta-c section-title--1__title" v-html="content.title" />
            <p class="no-margin ta-c section-title--1__subtitle" v-html="content.subtitle" />
        </template>
        <template  v-else-if="mode === '2'" >
            <h2 class="ta-c section-title--2__title" v-html="content.title" />
            <p class="no-margin ta-c section-title--2__subtitle" v-html="content.subtitle" />
        </template>
    </header>
</template>

<script>
export default {
    name: 'sectionTitle',

    props: {
        /**
         * Section title mode
         */
        mode: {
            type: String,
            default: '1',
        },

        /**
         * Section title content
         * get number from 1 to 2
         */
        content: Object,
    },

}
</script>
