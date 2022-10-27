<template> 
    <div>
        <header class="header">
            <div class="header__container">
                <div class="header__container__inner">
                    <nav class="header__container__inner__navbar">
                        <span class="header__container__inner__navbar__item">Каталог</span>
                        <span class="header__container__inner__navbar__item">Доставка</span>
                        <span class="header__container__inner__navbar__item">Оплата</span>
                        <span class="header__container__inner__navbar__item">Контакты</span>
                        <span class="header__container__inner__navbar__item">О&nbsp;компании</span>
                    </nav>
                    <div class="header__container__inner__search">
                        <input class="header__container__inner__search__input" placeholder="Поиск по названию картины" type="text" v-model="search">
                        <button class="header__container__inner__search__button">
                            <a href="#">Найти</a>
                        </button>
                    </div>
                </div>
            </div>
        </header>
        <main class="main">
            <p class="main__title">Картины эпохи Возрождения</p>
            <div class="main__container">
                <div v-for="card in filteredCards" :key="card.id">
                    <card :card="card"></card>
                </div>
            </div>
        </main>
    </div>
</template> 

<script>
import venera from '../static/venera.png'
import secretMeeting from '../static/secret-meeting.png'
import adam from '../static/adam.png'
import anatomy from '../static/anatomy.png'
import Card from "./Card.vue"

export default {
    name: "Main",
    components: { Card }, 
    data() {
        return { 
            search: "",
            cards: [
                {
                    id: 1,
                    image: venera,
                    title: "«Рождение Венеры» Сандро Боттичелли",
                    crossedOut: "2 000 000 $",
                    discount: "1 000 000 $"
                },
                {
                    id: 2,
                    image: secretMeeting,
                    title: "«Тайная вечеря» Леонардо да Винчи",
                    discount: "3 000 000 $"
                },
                {
                    id: 3,
                    image: adam,
                    title: "«Сотворение Адама» Микеланджело",
                    crossedOut: "6 000 000 $",
                    discount: "5 000 000 $"
                },
                {
                    id: 4,
                    image: anatomy,
                    title: "«Урок анатомии» Рембрандт",
                    discount: "2 500 000 $"
                }
            ]
        }
    },
    computed: {
        filteredCards() {
            return this.cards.filter(card => 
                card.title.toLowerCase().includes(this.search.toLowerCase())
            )
        }
    },
    methods: {
        saveSession() {
            this.loading-!false
            setTimeout(() => {
                this.loading-!true
            }, 2000)
        }
    }
}
</script>

<style>
    .header {
        padding: 0 auto;
    }
    .header__container {
        max-width: 1216px; 
        min-height: 97px;
        margin: 0 auto;
        padding: 0 15px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        border-bottom: 1px solid #E1E1E1;
    }
    .header__container__inner {
        width: 1120px;
        min-height: 97px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .header__container__inner__navbar {
        
    }
    .header__container__inner__navbar__item {
        margin: 15px;
        cursor: pointer; 
    }
    .header__container__inner__search {
        display: flex;
        align-items: center;
    }
    .header__container__inner__search__input {
        width: 290px;
        height: 44px;
        text-indent: 15px;
    }
    .header__container__inner__search__button {
        width: 122px;
        height: 48px;
        background-color: #403432;
    }
    .header__container__inner__search__button a {
        color: #fff;
    }
    .main {
        margin: 0 auto;
        padding: 0 15px;
        max-width: 1216px;
    }
    .main__title {
        margin-top: 40px;
        margin-bottom: 35px;
        font-size: 24px;
        font-weight: 700;
        color: #343030;
    }
    .main__container {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    .main__container__card {
        width: 280px;
        height: 328px;
        margin: 15px 10px;
        border: 1px solid #E1E1E1;
    }
    .main__container__card__img {
        
    }
    .main__container__card__title {
        padding-top: 20px;
        margin: 0 23px;
        font-size: 18px;
        color: #343030;
    }
    .main__container__card__buy {
        padding-top: 20px;
        margin: 0 23px;
        display: flex;
        justify-content: space-between;
    }
    .main__container__card__buy__price {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
    }
    .main__container__card__buy__price__crossed-out {
        font-size: 14px;
        font-weight: 300;
        color: #A0A0A0;
        text-decoration: line-through;
    }
    .main__container__card__buy__price__discount {
        font-size: 16px;
        color: #343030;
    }
    .main__container__card__buy__button {
        width: 118px;
        height: 48px;
        font-size: 14px;
        font-weight: 700;
        color: #F4F6F9;
        background-color: #382E2B;
    }

    @media(max-width: 1185px) {
        .header__container {
            height: 130px;
        }
        .header__container__inner {
            flex-wrap: wrap;
        }
        .header__container__inner__navbar {
            margin-right: 0;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        .header__container__inner__navbar__item {
            margin-right: 0;
        }
    }
    @media(max-width: 998px) {
        .header__container__inner {
            height: max-content;
            flex-direction: column;
            justify-content: center;
        }
    }
    @media(max-width: 600px) {
        .header {
            height: max-content;
        }
        .header__container {
            height: max-content;
        }
        .header__container__inner__search {
            margin-bottom: 15px;
        }
        .header__container__inner__search__input {
            width: 230px;
        }
        .header__container__inner__search__button {
            width: 80px;
        }
        .main__title {
            font-size: 19px;
        }
    }
</style>