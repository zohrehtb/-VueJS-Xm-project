<template>
    <header class="main-header">
        <a 
            class="main-header__logo" 
            href="#" 
            title="logo"
        >
            <img
                :src="require('../../assets/images/logo.png')"
                alt="XM"
            >
        </a>
        <nav class="main-header__menu d-none d-lg-block">
            <ul class="d-flex">
                <li 
                    v-for="(menuItem, index) in menuItems" 
                    :key="index"  
                    class="main-header__menu__item"
                >
                    <a 
                        :title="menuItem.title" 
                        :href="menuItem.link"
                    >
                        {{menuItem.title}}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'mainHeader',

    /**
     * @inheritDoc
     */
    data() {
        return {
            menuItems:[
                {
                    title:'XM Homepage',
                    link:'#',
                },
                {
                    title:'Support',
                    link:'#',
                }
            ]
        };
    },
};
</script>
