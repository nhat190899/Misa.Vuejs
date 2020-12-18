<template>
    <div class="grid">
        <div class="grid-content">
            <table>
                <thead>
                    <tr>
                        <th v-for="(column,index) in listColumn"
                            :key="index"
                            :fieldname="column.fieldname"
                        >
                            {{ column.value }}
                        </th>
                        <!--<th fieldname="EmployeeCode">Mã nhân viên</th>
                        <th fieldname="FullName">Họ và tên</th>
                        <th fieldname="GenderName">Giới tính</th>
                        <th fieldname="DateOfBirth" formatType="ddmmyyyy">Ngày sinh</th>
                        <th fieldname="PhoneNumber">Điện thoại</th>
                        <th fieldname="Email">Email</th>
                        <th fieldname="PositionName">Chức vụ</th>
                        <th fieldname="DepartmentName">Phòng ban</th>
                        <th fieldname="Salary" formatType="money">Mức lương cơ bản</th>
                        <th fieldname="StateName">Tình trạng công việc</th>-->
                    </tr>
                </thead>
                <tbody>
                    <!--<tr is="tr-employee"
                        v-for="(employee,index) in listEmployee"
                        :key="index"
                    >
                    </tr>-->
                </tbody>
            </table>
            <!--<div class="emptyBody">Không có dữ liệu phù hợp</div>-->
        </div>
        <div class="paging">
            <div class="page-info">Hiển thị 1-10/1000 nhân viên</div>
            <!--<div class="pages">
                <button class="previous-page square"></button>
                <button class="page-1 circle">1</button>
                <button class="page-2 circle">2</button>
                <button class="page-3 circle">3</button>
                <button class="page-4 circle">4</button>
                <button class="next-page square"></button>
            </div>-->
            <button class="total-page">10 trang</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Grid',
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
                ],
                listEmployee: [
                    {
                        EmployeeId: "0fad2b84-3621-11eb-b300-42010a8c0003",
                        EmployeeCode: "NV0010001",
                        FullName: "Trần Hoài Nhật",
                        DateOfBirth: null,
                        GenderId: "6528b15d-6674-724f-79a4-4b24de418577",
                        GenderName: "Nam ",
                        EmployeeIdentityCode: "312315",
                        DateOfLicense: null,
                        PlaceOfLicense: "",
                        Email: "nhat190899@gmail.com",
                        PhoneNumber: "312312",
                        PositionId: "6fd9cee5-30b5-5670-79ff-f8ad76748b41",
                        PositionName: "Nhân viên Marketting",
                        DepartmentId: "3f8e6896-4c7d-15f5-a018-75d8bd200d7c",
                        DepartmentName: "Phòng marketting",
                        EmployeeTaxCode: "",
                        Salary: 4500000.0,
                        DateJoin: null,
                        StateId: "30d41e52-5e66-72bc-6c1c-b47866e0b131",
                        StateName: "Đang thử việc",
                        EntityState: 0,
                    },
                    {
                        EmployeeId: "f76f8c1f-3620-11eb-b300-42010a8c0003",
                        EmployeeCode: "NV0010000",
                        FullName: "Trần Hoài Nhật",
                        DateOfBirth: null,
                        GenderId: "6528b15d-6674-724f-79a4-4b24de418577",
                        GenderName: "Nam ",
                        EmployeeIdentityCode: "312315",
                        DateOfLicense: null,
                        PlaceOfLicense: "",
                        Email: "nhat190899@gmail.com",
                        PhoneNumber: "24123",
                        PositionId: "6fd9cee5-30b5-5670-79ff-f8ad76748b41",
                        PositionName: "Nhân viên Marketting",
                        DepartmentId: "3f8e6896-4c7d-15f5-a018-75d8bd200d7c",
                        DepartmentName: "Phòng marketting",
                        EmployeeTaxCode: "",
                        Salary: 4500000.0,
                        DateJoin: null,
                        StateId: "30d41e52-5e66-72bc-6c1c-b47866e0b131",
                        StateName: "Đang thử việc",
                        EntityState: 0,
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    @import '../css/grid.css';
</style>