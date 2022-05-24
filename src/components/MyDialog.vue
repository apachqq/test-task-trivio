<template>
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
</template>

<script>
    export default {
        data() {
            return {
                balance: '-597 771, 77',
                debt: '0, 00'
            }
        },
        props: {
            isOpen: {
                type: Boolean
            }
        }
    }
</script>

<style lang="scss" scoped>
    .dialog {
        display: flex;
        background-color: white;
        flex-direction: column;
        position: absolute;
        bottom: 478px;
        left: 1670px;
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
            cursor: pointer;
        }

        span:nth-child(8) {
            padding: 10px 10px 5px;
            color: red;
            cursor: pointer;
        }
    }

    @media screen and (max-width: 1059px) {
        .dialog {
            display: flex;
            flex-direction: column;
            position: absolute;
            left: 780px;
            width: 150px;
            box-shadow: 2px 2px 2px 2px rgba(0, 0, 0, 0.2);
            border: none;
            z-index: 1;
        }
    }

    @media screen and (max-width: 882px) {
        .dialog {
            left: 325px;
        }
    }

    @media screen and (max-width: 550px) {
        .dialog {
            left: 165px;
        }
    }

    @media screen and (max-width: 420px) {
        .dialog {
            bottom: 575px;
        }
    }
</style>
