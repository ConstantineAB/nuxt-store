<template>
    <div class="main__container__card">
        <div class="main__container__card__img">
            <img :src="card.image" alt="img">
        </div>
        <p class="main__container__card__title">
            {{card.title}}
        </p>
        <div class="main__container__card__buy">
            <div class="main__container__card__buy__price">
                <p class="main__container__card__buy__price__crossed-out">
                    {{card.crossedOut}}
                </p>
                <p class="main__container__card__buy__price__discount">
                    {{card.discount}}
                </p>
            </div>
            <Button />
        </div>
    </div>
</template>

<script>
import Button from "./Button.vue"

export default {
    props: ["card"],
    components: { Button },
    data() {
        return {

        }
    }
}
</script>

<style scoped>

</style>
