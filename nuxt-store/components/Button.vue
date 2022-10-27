<template>
    <button @click="clickBuy()" class="main__container__card__buy__button">
        <Spinner v-if="loading" />
        <span v-if="!loading">
            <p>{{text}}</p>
        </span>
    </button>
</template>

<script>
import Spinner from "./Spinner.vue"


export default {
    props: ["card"],
    components: { Spinner },
    data() {
        return {
            loading: false,
            basketIsFull: false,
            text: "Купить"
        }
    },
    methods: {
        clickBuy() {
            this.loading=!false
            setTimeout(() => {
                this.loading=!true
                this.basketIsFull = !this.basketIsFull
                if (this.basketIsFull === !false) {
                    this.text="В корзине"
                } else {
                    this.text="Купить"
                }
            }, 2000)
        }
    }
}
</script>

<style scoped>

</style>