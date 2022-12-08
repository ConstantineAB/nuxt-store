<template>
    <div class="footer">
        <div class="footer__container">
            <div class="footer__container__navbar">
                <span class="footer__container__navbar__item">
                    Каталог
                </span>
                <span class="footer__container__navbar__item">
                    Доставка
                </span>
                <span class="footer__container__navbar__item">
                    Оплата
                </span>
                <span class="footer__container__navbar__item">
                    Контакты
                </span>
                <span class="footer__container__navbar__item">
                    О&nbsp;компании
                </span>
            </div>
            <div class="footer__container__contacts">
                <div class="footer__container__contacts__phone">
                    <span class="footer__container__contacts__phone__img">
                        <img src="../static/icons/phone.png" alt="phone">
                    </span>
                    <span class="footer__container__contacts__phone__text">
                        +7 (812) 555-55-55
                    </span>
                </div>
                <div class="footer__container__contacts__address">
                    <span class="footer__container__contacts__address__img">
                        <img src="../static/icons/adress.png" alt="address">
                    </span>
                    <span class="footer__container__contacts__address__text">
                        г. Санкт-Петербург, ул. Ефимова, 3
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

</script>

<style>
    .footer {
        height: max-content;
        display: flex;
        align-items: center;
        background-color: #ECEAEA;
    }
    .footer__container {
        margin: 0 auto;
        padding: 0 15px;
        width: 1216px;
        height: max-content;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
    }
    .footer__container__navbar {
        padding: 15px 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        height: max-content;
    }
    .footer__container__navbar__item {
        margin: 0 15px;
        line-height: 30px;
        color: #555555;
    }
    .footer__container__contacts {
        display: flex;
        flex-wrap: wrap;
    }
    .footer__container__contacts__phone {
        padding: 25px 5px;
    }
    .footer__container__contacts__phone__img {
        
    }
    .footer__container__contacts__phone__text {
        color: #555555;
    }
    .footer__container__contacts__address {
        padding: 25px 5px;
    }
    .footer__container__contacts__address__img {
        
    }
    .footer__container__contacts__address__text {
        color: #555555;
    }

</style>