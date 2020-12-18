<template>
    <div class="navbar">
        <Logo></Logo>
        <Menu></Menu>
    </div>
</template>

<script>

    import Logo from './Logo.vue'
    import Menu from './Menu.vue'
    export default {
        name: 'Navbar',
        components: {
            Logo,
            Menu
        }
    }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import '../css/navbar.css';
</style>