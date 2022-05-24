<template>
    <the-header
            :isOpen="isOpen"
            @close="closeMyDialog"
    ></the-header>
    <my-body
            @click="isOpen = false"
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
            closeMyDialog() {
                this.isOpen = !this.isOpen
            }
        },
        components: {TheHeader, MyDialog, MyBody}
    }
</script>

<style lang="scss">
</style>
