<template>
  <div v-if="content && content.length" class="contact-us">
        <div class="contact-us__items row">
            <b-col md="4" class="contact-us__item">
                <i class="fa fa-calendar-check-o" aria-hidden="true"></i>
                <span class="ta-c">{{content.date}}</span>
            </b-col>
            <b-col md="4" class="contact-us__item">
                <i class="fa fa-clock-o" aria-hidden="true"></i>
                <span class="ta-c">1{{content.time}}</span>
            </b-col>
            <b-col md="5" class="contact-us__item">
                <i class="fa fa-map-marker" aria-hidden="true"></i>
                <span class="ta-c">{{content.location}}</span>
            </b-col>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ContactUs',

    data(){
        return{ 
            content:{
                date:'12 NOVEMBER 2022',
                time:'6:00 – 23:00',
                location:'Centara Grand & Bangkok Convention Centre, Bangkok',
            }
        }
    },

}
</script>
