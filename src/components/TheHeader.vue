<template>
    <div class="main">
        <a href="#" class="logo"><img src="img/logo.svg"></a>
        <div class="left-header">
            <a href="#" class="word-left" v-for="inscription in leftHeader" :key="inscription.id">{{ inscription.title
                }}</a>
            <a href="#" style="margin-left: 10px; border-radius: 8px; background-color: darkgrey; padding: 5px 5px">Пакеты услуг</a>
        </div>
        <div class="right-header">
            <a href="#" class="word-right"><img src="img/login.svg"></a>
            <a href="#" class="word-right"><img src="img/twit-logo.svg"></a>
            <a href="#" class="word-right"><img src="img/odnokl-logo.svg"></a>
            <a href="#" class="word-right"><img src="img/inst-logo.svg"></a>
            <a href="#" class="word-right" @click.prevent="$emit('close')"><img src="img/registration.svg"></a>
            <a href="#" class="word-right"><img src="img/vk-logo.svg"></a>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                leftHeader: [
                    {id: 1, title: 'Рабочий стол'},
                    {id: 2, title: 'Проекты'},
                    {id: 3, title: 'Оплаты'},
                    {id: 4, title: 'Моя компания'},
                    {id: 5, title: 'Финансы'}
                ]
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
    .main {
        display: flex;
        box-shadow: 1px 1px 1px 1px rgba(0, 0, 0, 0.2);

        .left-header {
            display: flex;
            align-items: center;
            margin-left: 20px;

            a {
                text-decoration: none;
                color: black;
                display: block;
                overflow: hidden;
                transition: 1s;

                &:hover {
                    transform: scale(1.1);
                }
            }

            .logo {
                padding: 0.5rem 1.5rem;
            }

            .word-left {
                margin-left: 10px;
            }
        }

        .right-header {
            display: flex;
            align-items: center;
            margin-left: auto;

            a {
                display: block;
                overflow: hidden;
                transition: 1s;

                &:hover {
                    transform: scale(1.1);
                }
            }

            .word-right {
                padding-right: 0.7rem;
            }
        }
    }

    @media screen and (max-width: 882px) {
        .main {
            flex-direction: column;

            .logo {
                margin: auto auto;
            }

            .left-header {
                margin: auto auto;
                padding: 10px 0 10px;
            }

            .right-header {
                margin: auto auto;
            }
        }
    }

    @media screen and (max-width: 550px) {
        .left-header {
            flex-wrap: wrap;
            justify-content: center;
        }
    }
</style>
