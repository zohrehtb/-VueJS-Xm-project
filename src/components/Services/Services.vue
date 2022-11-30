<template>
  <div v-if="items && items.length" class="services">
        <div 
            v-for="item in items" 
            :key="item.id" 
            class="services__item"
        >
            <img class="services__item__img" 
                :src="require(`../../assets/images/${item.image}`)" 
                :alt="item.title"
            />
            <h3 class="services__item__title">{{item.title}}</h3>
            <p class="services__item__text">{{item.synapsis}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name:'CServices',

    props:{
        items:Array,
    }
}
</script>
