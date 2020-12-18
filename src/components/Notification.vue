<template>
    <div>
        <div class="notification" id="notiSuccess" style="display: none;"></div>
        <div class="notification" id="notiFail" style="display: none;"></div>
        <div id="confirmForm" style="display: none;">
            <div class="confirmForm-title">
                <div class="confirmForm-title-text">Xóa bản ghi</div>
                <div class="confirmForm-iconClose"></div>
            </div>
            <div class="confirmForm-content">
                <div class="iconWarn"></div>
                <div class="confirmForm-content-text"></div>
            </div>
            <div class="confirmForm-button">
                <button class="btnDelete">Có</button>
                <button class="btnCancel">Không</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Notification'
    }
</script>

<style scoped>
    @import '../css/notification.css';
</style>