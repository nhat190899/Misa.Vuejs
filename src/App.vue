<template>
    <div id="app">
        <div>
            <Navbar></Navbar>
            <Header></Header>
            <Content @add-employee="addEmployee"></Content>
            <Notification></Notification>
            <Dialog
                    v-show="dialogState"
                    @close-dialog="closeDialog"></Dialog>
            <Loading></Loading>
        </div>
        <div class="cover" v-bind:class="{modal:isAppModal}"></div>
    </div>
</template>

<script>
    import Navbar from './components/Navbar.vue'
    import Header from './components/Header.vue'
    import Content from './components/Content.vue'
    import Notification from './components/Notification.vue'
    import Dialog from './components/Dialog.vue'
    import Loading from './components/Loading.vue'

    export default {
        name: 'App',
        components: {
            Navbar,
            Header,
            Content,
            Notification,
            Dialog,
            Loading
        },
        data() {
            return {
                dialogState: false,
                formMode: 'POST',
                isAppModal: false,
            }
        },
        methods: {
            addEmployee() {
                debugger; //eslint-disable-line no-debugger
                this.dialogState = true;
                this.formMode = 'POST';
                this.isAppModal = true;
            },
            closeDialog() {
                this.dialogState = false;
                this.isAppModal = false;
            }
        }
    }

</script>

<style scoped>
    @import './css/main.css';
</style>
