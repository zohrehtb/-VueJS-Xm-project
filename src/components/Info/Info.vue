<template>
   <section v-if="items && items.length" class="info">
        <div class="info__col1">
            <div class="info-card info-card--fast">
                <h2 class="info-card__title">{{items[0].title}}</h2>
                <p class="info-card__synapsis">{{items[0].synapsis}}</p>
            </div>
        </div>
        <div class="info__col2">
            <div class="info-card info-card--pricing">
                <h2 class="info-card__title info-card__title">{{items[1].title}}</h2>
                <p class="info-card__synapsis">{{items[1].synapsis}}</p>
            </div>
            <div class="info__row">
                <div class="info__row__col">
                    <div class="info-card info-card--tech">
                        <h2 class="info-card__title info-card__title">{{items[2].title}}</h2>
                        <p class="info-card__synapsis">{{items[2].synapsis}}</p>
                    </div>
                </div>
                <div class="info__row__col">
                    <div class="info-card info-card--dollar">
                        <h2 class="info-card__title info-card__title">{{items[3].title}}</h2>
                        <p class="info-card__synapsis">{{items[3].synapsis}}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'CInfo',

    data(){
        return{ 
            items:[
                {
                    id:'1',
                    title:'Superior Trade Execution',
                    synapsis:'99% of trades are executed in less than a second, with no requotes or rejections.',
                },
                {
                    id:'2',
                    title:'Competitive Pricing',
                    synapsis:'We offer some of the lowest spreads and we don’t charge commissions.',
                },
                {
                    id:'3',
                    title:'Advanced Technology',
                    synapsis:'Trade on MT4 or MT5, with expert tools, across desktop, web and mobile.',
                },
                {
                    id:'4',
                    title:'Start with $5',
                    synapsis:'Start trading your preferred instruments with as little as a $5 minimum deposit.',
                },
            ]
        }
    },
}
</script>