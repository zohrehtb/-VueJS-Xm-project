<template>
  <section v-if="hero" class="hero">
        <b-container>
            <div class="hero__content">
                <span class="hero__title2 ta-c">{{hero.title2}}</span>

                <h1 
                    class="hero__title ta-c" 
                    v-html="hero.title"
                />

                <p 
                    class="hero__synapsis ta-c" 
                    v-html="hero.synapsis"
                />

                <button class="submit">open account</button>

                <p class="hero__sublink1 ta-c">
                    New to trading? Try a
                    <a title="Demo" href="#">Demo account</a>.
                </p>

                <p class="hero__sublink2 ta-c">
                    Terms and Conditions apply<span>*</span>. To read the full T&Cs,
                    <a title="button" href="#">click here.</a>
                </p>
            </div>
        </b-container>
    </section>
</template>

<script>

export default {
    name: 'CHero',

    data(){
        return{ 
            hero:{
                title2:'trade with',
                title:'<strong>Zero Swaps</strong> on All XM Ultra Low Accounts for more than 25 instruments!',
                synapsis:' Enjoy spreads <strong>as low as 0.6 pips</strong> and <strong>leverage up to 1000:1</strong> on instruments like<strong>EURUSD, USDJPY, EURJPY, GBPUSD,</strong> and <strong>Gold</strong>.',
            }
        }
    },
}

</script>