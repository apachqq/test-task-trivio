<template>
    <the-header
            :isOpen="isOpen"
            @close="closeOpenMyDialog"
    ></the-header>
    <my-body
            @click="closeMyDialog"
    ></my-body>
    <my-dialog style="position: relative"
               :isOpen="isOpen"
    ></my-dialog>
</template>

<script>
    import TheHeader from '@/components/TheHeader'
    import MyDialog from '@/components/MyDialog'
    import MyBody from '@/components/MyBody'

    export default {
        data() {
            return {
                isOpen: false
            }
        },
        methods: {
            closeOpenMyDialog() {
                this.isOpen = !this.isOpen
            },
            closeMyDialog() {
                this.isOpen = false
            }
        },
        components: {TheHeader, MyDialog, MyBody}
    }
</script>

<style lang="scss">
</style>
