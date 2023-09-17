<template>
    <div class="card__content">
        <div class="card__flex">
            <div class="card-self" :class="{ active: card.isActive}"
                v-for="card in cards" :key="card.id"
                @click="changeVisibility(card.id)">
                <img v-if="card.visible" :src="card.path" alt="card">
                <img v-else :src="card.open" alt="card">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyCards',

    data() {
        return {
            cards: [
                {
                    id: 1,
                    path: require('../assets/images/card.png'),
                    open: require('../assets/images/open-card.png'),
                    isActive: false,
                    visible: true,
                },
                {
                    id: 2,
                    path: require('../assets/images/card.png'),
                    open: require('../assets/images/open-card.png'),
                    isActive: true,
                    visible: false,
                },
                {
                    id: 3,
                    path: require('../assets/images/card.png'),
                    open: require('../assets/images/open-card.png'),
                    isActive: false,
                    visible: true,
                },
            ]
        };
    },

    mounted() {
        
    },

    methods: {
        changeVisibility(id) {
            this.cards[id-1].isActive = !this.cards[id-1].isActive;

            setTimeout(() => {
                this.cards[id-1].visible = !this.cards[id-1].visible
            }, 300)
        }
    },
};
</script>

<style lang="scss" scoped>

</style>