<template>
  <section v-if="items && items.length">
        <b-container>
             <div class="crypto-widgets">
                <div
                    v-for="item in filterItems"
                    :key="item.id"
                    class="crypto-widgets__item"
                >
                    <header class="crypto-widgets__item__header">
                        <img 
                            class="crypto-widgets__item__img" 
                            :src="require(`../../assets/images/w_${item.symbol}.png`)"
                            :alt="item.symbol"
                        >
                        <h5 class="crypto-widgets__item__symbol">{{item.symbol}}</h5>
                        <span class="crypto-widgets__item__name">{{item.name}}</span>
                    </header>
                    <div class="crypto-widgets__item__prices">
                        <span class="crypto-widgets__item__usd-price">
                            <i class="fa fa-usd" aria-hidden="true"></i>{{item.price_usd}}
                        </span>
                        <span class="crypto-widgets__item__percent">
                            {{item.percent_change_1h}}
                        </span>
                    </div>
                </div>
             </div>
        </b-container>
    </section>
</template>

<script>

export default {
    name: 'WCrypto',

    data(){
        return{ 
            items:null,
        }
    },

    mounted() {
      this.getData()
    },

    computed: {
        /**
         * Filter items
         */
        filterItems() {
            const selectedItems = [];

            this.items.forEach((item) => {
                if (item.symbol == 'BTC' || item.symbol =='ETH' || item.symbol =='XRP' || item.symbol =='LTC' || item.symbol =='BCH') {
                    selectedItems.push(item);
                }
            });

            return selectedItems;
        },
    },

    methods: {
      async getData() {
        const responses = await fetch("https://api.coinlore.net/api/tickers/");
        const finalResponses = await responses.json();
        this.items = finalResponses.data;
      }
    }
}

</script>