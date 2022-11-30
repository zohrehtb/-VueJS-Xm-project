<template>
    <main>
        <c-hero />
        <crypto-widgets />
        <b-container>
            <section-title :content="sectionTitle1"/>
            <c-info />
        </b-container>
        <b-container>
            <section-title :content="sectionTitle2" mode="2" />
            <contact-us />
            <c-register />
        </b-container>
        <c-gallery :items="gallery" />
        <div class="about-us">
             <b-container>
               <b-row>
                <b-col xl="3">
                    <our-motto :content="motto"/>
                </b-col>
                <b-col xl="9">
                    <c-services :items="services"/>
                </b-col>
               </b-row>
             </b-container>
        </div>
    </main>
</template>

<script>

import CHero from '../components/Hero/Hero.vue'
import CInfo from '../components/Info/Info.vue'
import CGallery from '../components/Gallery/Gallery.vue'
import OurMotto from '../components/OurMotto/OurMotto.vue'
import CRegister from '../components/Register/Register.vue'
import CServices from '../components/Services/Services.vue'
import ContactUs from '../components/ContactUs/ContactUs.vue'
import SectionTitle from '../components/SectionTitle/SectionTitle.vue'
import CryptoWidgets from '../components/CryptoWidgets/CryptoWidgets.vue'

export default {
name: 'homePage',

    components: {
        CHero,
        CInfo,
        OurMotto,
        CGallery,
        CRegister,
        ContactUs,
        CServices,
        SectionTitle,
        CryptoWidgets
    },

    data(){
        return{ 
            sectionTitle1:{
                title:'Why <span>Trade</span> with XM?',
                subtitle:' We have been providing traders around the world with the same <strong>premium experience</strong> for over a decade. As an<strong>industry-leader</strong>, we know what the modern trader needs to be <strong>successful</strong> in the markets.',
            },
            sectionTitle2:{
                title:'- Register Here -',
                subtitle:'Join us to celebrate our biggest night of the year.',
            },
            motto:{
                customFields:{
                    title1:'Big',
                    title2:'Fair',
                    title3:'Human'
                },
                subtitle:'Learn why <strong>over 5 million clients choose XM</strong> as their trusted online broker.',
            },
            services:[
                {
                    id:1,
                    image:'services4.png',
                    title:'Authorised and Regulated',
                    synapsis:'At XM, we adhere to all regulatory standards and are fully authorised and regulated by FSC.',
                },
                {
                    id:2,
                    image:'services1.png',
                    title:'Committed and Fair',
                    synapsis:'We operate with complete transparency and adhere to the highest professional and ethical standards.',
                },
                {
                    id:3,
                    image:'services2.png',
                    title:'Multi-Award-Winning',
                    synapsis:'Over the years we have received over 40 awards for the quality of our products and services.',
                },
                {
                    id:4,
                    image:'services3.png',
                    title:'24/7 Support',
                    synapsis:'Our support agents are on hand 24/7 to answer your questions or assist you with any issues.',
                },
            ],
            gallery:[
                {
                    id:1,
                    image:'gallery.png',
                    title:'Event gallery title',
                },
                {
                    id:2,
                    image:'gallery.png',
                    title:'Event gallery title',
                },
                {
                    id:3,
                    image:'gallery.png',
                    title:'Event gallery title',
                },
                {
                    id:4,
                    image:'gallery.png',
                    title:'Event gallery title',
                },
                {
                    id:5,
                    image:'gallery.png',
                    title:'Event gallery title',
                },
            ]
        }
    },

    methods: {

        

    }
}
</script>
