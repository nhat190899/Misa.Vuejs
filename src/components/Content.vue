<template>
    <div class="content">
        <div class="title">
            <div class="title-text">Danh sách nhân viên</div>
            <button class="title-popup">
                <div class="title-popup-text" id="btnAdd" @click="addEmployee">
                    <div class="adduser-icon"></div>
                    <div class="text">Thêm nhân viên</div>
                </div>
            </button>
        </div>
        <div class="filter">
            <div class="filter-left">
                <input type="search" class="search-type" id="txtSearch" placeholder="Tìm kiếm theo Mã, Tên hoặc Số điện thoại" />
                <select id="cxbDepartment">
                    <option>Tất cả phòng ban</option>
                </select>
                <select id="cxbPosition">
                    <option>Tất cả vị trí</option>
                </select>
            </div>
            <div id="btnRefresh" class="refresh-icon"></div>
        </div>
        <Grid></Grid>
    </div>
</template>

<script>
    import axios from 'axios'
    import Grid from './Grid.vue';
    export default {
        name: 'Content',
        components: {
            Grid
        },
        data() {
            return {
                api: null
            }
        },
        mounted() {
            this.loadTable();
        },
        methods: {
            addEmployee() {
                this.$emit('add-employee');
            },
            loadTable() {
                axios.get('https://localhost:44308/api/v1/Employees/0fad2b84-3621-11eb-b300-42010a8c0003')
                    .then((response) => (this.api = response.data)) //eslint-disable-line no-debugger
                    .catch(error => console.log(error)) //eslint-disable-line no-debugger
                debugger; //eslint-disable-line no-debugger
            }
        }
    }
</script>

<style scoped>
    @import '../css/content.css';
</style>