<template>
    <footer class="main-footer">
        <div class="main-footer__p1 d-none d-lg-flex">
            <div 
                v-if="customers && customers.length"
                class="our-customer d-flex"
            >
                <a 
                    v-for="(customer, index) in customers" 
                    :key="index" 
                    class="our-customer__items" 
                    :href="customer.link"
                    :title="customer.title"
                >
                    <img :src="require(`../../assets/images/${customer.image}`)" :alt="customer.title"/>
                </a>
            </div>

            <div class="socials d-flex">
                <span class="socials__title">Follow us on</span>
                <nav>
                    <ul class="d-flex">
                        <li class="socials__item">
                            <a href="#" title="facebook">
                                <font-awesome-icon icon="fa-brands fa-facebook" />
                            </a>
                        </li>
                        <li class="socials__item">
                            <a href="#" title="twitter">
                                <font-awesome-icon icon="fa-brands fa-twitter" />
                            </a>
                        </li>
                        <li class="socials__item">
                            <a href="#" title="youtube">
                                <font-awesome-icon icon="fa-brands fa-youtube" />
                            </a>
                        </li>
                        <li class="socials__item">
                            <a href="#" title="instagram">
                                <font-awesome-icon icon="fa-brands fa-instagram" />
                            </a>
                        </li>
                        <li class="socials__item">
                            <a href="#" title="linkedin">
                                <font-awesome-icon icon="fa-brands fa-linkedin" />
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>

        <div class="main-footer__p2 row">
            <nav class="main-footer__menu col-md-8">
                <ul
                    v-if="menuItems && menuItems.length"
                    class="d-flex">
                    <li
                        v-for="(menuItem, index) in menuItems"
                        :key="index"
                        class="main-footer__menu__items"
                    >
                        <a :href="menuItem.link" :title="menuItem.title">{{menuItem.title}}</a>
                        <span
                            v-if="index < menuItems.length - 1"
                            class="sp"
                        >
                            |
                        </span>
                    </li>
                </ul>
            </nav>
            <a class="main-footer__logo col-md-4" href="#">
                <img :src="require('../../assets/images/f-logo.png')" alt="logo"/>
            </a>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'mainFooter',

    /**
     * @inheritDoc
     */
    data() {
        return {
            customers:[
                {
                    title:'customers4',
                    image:'f-customers4.png',
                },
                {
                    title:'customers2',
                    image:'f-customers3.png',
                },
                {
                    title:'customers2',
                    image:'f-customers2.png',
                },
                {
                    title:'customers1',
                    image:'f-customers1.png',
                }
            ],

            menuItems:[
                {
                    title:'Privacy Policy',
                    link:'#',
                },
                {
                    title:'Cookie Policy',
                    link:'#',
                },
                {
                    title:'Terms and Conditions',
                    link:'#',
                }
            ]
        };
    },

}
</script>
