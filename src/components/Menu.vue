<template>
    <div class="menu">
        <a href="electronic_document.html" class="menu-item">
            <div class="menu-item-icon edoc-icon"></div>
            <div class="menu-item-text">Lập hồ sơ điện tử</div>
        </a>
        <a href="paper_document.html" class="menu-item">
            <div class="menu-item-icon doc-icon"></div>
            <div class="menu-item-text">Lập hồ sơ giấy</div>
        </a>
        <a href="pay_chart.html" class="menu-item">
            <div class="menu-item-icon chart-icon"></div>
            <div class="menu-item-text">Theo dõi chi</div>
        </a>
        <a href="employee.html" class="menu-item">
            <div class="menu-item-icon cone-icon"></div>
            <div class="menu-item-text">Quản lý nhân viên</div>
        </a>
        <a href="customer.html" class="menu-item">
            <div class="menu-item-icon group-icon"></div>
            <div class="menu-item-text">Quản lý khách hàng</div>
        </a>
        <a href="setting.html" class="menu-item">
            <div class="menu-item-icon setting-icon"></div>
            <div class="menu-item-text">Thiết lập</div>
        </a>
    </div>
</template>

<script>
    export default {
        name: 'Menu'
    }
</script>

<style scoped>
    @import '../css/menu.css';
</style>