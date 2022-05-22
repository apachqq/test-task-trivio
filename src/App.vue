<template>
    <div>
        <div class="main">
            <div class="left-header">
                <div class="logo"><img src="img/logo.svg"></div>
                <div class="word-left">Рабочий стол</div>
                <div class="word-left">Лллллл</div>
                <div class="word-left">Оплаты</div>
                <div class="word-left">Моя компания</div>
                <div class="word-left">Финансы</div>
            </div>
            <div class="right-header">
                <div class="word-right"><img src="img/login.svg"></div>
                <div class="word-right"><img src="img/twit-logo.svg"></div>
                <div class="word-right"><img src="img/odnokl-logo.svg"></div>
                <div class="word-right"><img src="img/inst-logo.svg"></div>
                <div class="word-right" @click="isOpen = !isOpen"><img src="img/registration.svg"></div>
                <div class="word-right"><img src="img/vk-logo.svg"></div>
            </div>
        </div>
        <div class="dialog" v-if="isOpen">
            <span>admin admin</span>
            <span>Тривио</span>
            <span>баланс: {{ balance }} &#8381;</span>
            <span>задолженность: {{ debt }} &#8381;</span>
            <span>Профиль</span>
            <span>Управление</span>
            <span>Моя компания</span>
            <span>Выйти</span>
        </div>
        <div class="center">
            <div>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi blanditiis harum iste nulla, recusandae
                soluta tempora.
                Amet autem dolorem eligendi expedita itaque, iusto libero minus nemo pariatur, possimus soluta
                veritatis.
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                isOpen: true,
                balance: '-597 771, 77',
                debt: '0, 00'
            }
        }
    }
</script>

<style lang="scss">
    * {
        padding: 0;
        margin: 0;
    }

    .center {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        div {
            padding-top: 5rem;
            max-width: 400px;
        }
    }

    .dialog {
        display: flex;
        flex-direction: column;
        position: fixed;
        right: 10px;
        margin-left: auto;
        margin-right: 30px;
        margin-top: 0;
        width: 200px;
        box-shadow: 2px 2px 2px 2px rgba(0, 0, 0, 0.2);
        border: none;

        span:nth-child(1) {
            font-weight: bold;
            font-size: 15px;
            padding: 10px 10px;
        }

        span:nth-child(2),
        span:nth-child(3),
        span:nth-child(4) {
            color: darkgrey;
            font-size: 13px;
            padding-left: 10px;
        }

        span:nth-child(4) {
            padding-bottom: 10px;
        }

        span:nth-child(5),
        span:nth-child(6),
        span:nth-child(7) {
            padding-left: 10px;
            padding-bottom: 5px;
        }

        span:nth-child(8) {
            padding: 10px 10px 5px;
        }
    }

    .main {
        display: flex;
        justify-content: space-between;
        box-shadow: 1px 1px 1px 1px rgba(0, 0, 0, 0.2);

        .right-header {
            display: flex;
            align-items: center;

            .word-right {
                padding-right: 0.7rem;
            }
        }

        .left-header {
            display: flex;
            align-items: center;

            .logo {
                padding: 0.5rem 1.5rem;
            }

            .word-left {
                padding-left: 1rem;
            }
        }
    }
</style>
