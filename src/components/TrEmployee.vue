<template>
    <td is="td-employee"
        <!--v-for="(column,index) in listColumn"
        :key="index"
        :fieldname="column.fieldname"-->
    >
    </td>
</template>

<script>
    export default {
        name: 'TrEmployee',
        data() {
            return {
                listColumn: [
                    {
                        fieldname: "EmployeeCode",
                        value: "Mã nhân viên"
                    },
                    {
                        fieldname: "FullName",
                        value: "Họ và tên"
                    },
                    {
                        fieldname: "GenderName",
                        value: "Giới tính"
                    },
                    {
                        fieldname: "DateOfBirth",
                        value: "Ngày sinh"
                    },
                    {
                        fieldname: "PhoneNumber",
                        value: "Điện thoại"
                    },
                    {
                        fieldname: "Email",
                        value: "Email"
                    },
                    {
                        fieldname: "PositionName",
                        value: "Chức vụ"
                    },
                    {
                        fieldname: "DepartmentName",
                        value: "Phòng ban"
                    },
                    {
                        fieldname: "Salary",
                        value: "Mức lương cơ bản"
                    },
                    {
                        fieldname: "StateName",
                        value: "Tình trạng công việc"
                    }
                ]
            }
        }
    }
</script>

<style>

</style>