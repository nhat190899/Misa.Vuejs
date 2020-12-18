<template>
    <div class="dialog">
        <div class="dialog-header">
            <div class="title">THÔNG TIN NHÂN VIÊN</div>
            <div class="close-icon" @click="closeDialog"></div>
        </div>
        <div class="dialog-content">
            <div class="avatar">(Vui lòng chọn ảnh có định dạng<b> .jpg, .jpeg, .png, .gif)</b></div>
            <div class="detail">
                <div>A.THÔNG TIN CHUNG:</div>
                <div class="subtitle"></div>
                <div class="inline">
                    <div>
                        <label for="Employee-code">Mã nhân viên (<span style="color:red">*</span>)</label>
                        <input type="text" name="Employee-code" id="txtEmployeeCode" fieldname="EmployeeCode" required>
                    </div>
                    <div class="right">
                        <label for="txtFullName">Họ và tên (<span style="color:red">*</span>)</label>
                        <input type="text" name="idcard-code" id="txtFullName" fieldname="FullName" required>
                    </div>
                </div>

                <div class="inline">
                    <div>
                        <label for="dtDateOfBirth">Ngày sinh</label>
                        <input type="date" name="dtDateOfBirth" id="dtDateOfBirth" fieldname="DateOfBirth" placeholder="mm/dd/yyyy">
                    </div>
                    <div class="right">
                        <label for="Gender">Giới tính</label>
                        <select name="Gender" id="Gender" fieldname="GenderId">
                        </select>
                    </div>
                </div>
                <div class="inline">
                    <div>
                        <label for="EmployeeIdentityCode">Số CMTND/ Căn cước(<span style="color:red">*</span>)</label>
                        <input type="text" name="EmployeeIdentityCode" id="EmployeeIdentityCode" fieldname="EmployeeIdentityCode" required>
                    </div>
                    <div class="right">
                        <label for="dtDateOfLicense">Ngày cấp</label>
                        <input type="date" name="DateOfLicense" id="dtDateOfLicense" fieldname="DateOfLicense" placeholder="mm/dd/yyyy">
                    </div>
                </div>
                <div class="inline">
                    <div>
                        <label for="txtPlaceOfLicense">Nơi cấp</label>
                        <input type="text" name="PlaceOfLicense" id="txtPlaceOfLicense" fieldname="PlaceOfLicense">
                    </div>
                </div>
                <div class="inline">
                    <div>
                        <label for="txtEmail">Email (<span style="color:red">*</span>)</label>
                        <input type="email" name="txtEmail" id="txtEmail" fieldname="Email">
                    </div>
                    <div class="right">
                        <label for="txtPhoneNumber">Số điện thoại (<span style="color:red">*</span>)</label>
                        <input type="text" name="txtPhoneNumber" id="txtPhoneNumber" required fieldname="PhoneNumber">
                    </div>
                </div>
                <div class="second-title">B.THÔNG TIN CÔNG VIỆC:</div>
                <div class="subtitle"></div>
                <div class="inline">
                    <div>
                        <label for="dtPosition">Vị trí</label>
                        <select name="Position" id="dtPosition" fieldname="PositionId">
                        </select>
                    </div>
                    <div class="right">
                        <label for="dtDepartment">Phòng ban</label>
                        <select name="Department" id="dtDepartment" fieldname="DepartmentId">
                        </select>
                    </div>
                </div>
                <div class="inline">
                    <div>
                        <label for="txtEmployeeTaxCode">Mã số thuế cá nhân</label>
                        <input type="text" name="EmployeeTaxCode" id="txtEmployeeTaxCode" fieldname="EmployeeTaxCode">
                    </div>
                    <div class="right">
                        <label for="txtSalary">Mức lương cơ bản</label>
                        <input type="text" name="Salary" id="txtSalary" fieldname="Salary" pattern="^\$\d{1,3}(,\d{3})*(\.\d+)?$" data-type="currency" placeholder="(VND)">
                    </div>
                </div>
                <div class="inline">
                    <div>
                        <label for="dtDateJoin">Ngày gia nhập công ty</label>
                        <input type="date" name="DateJoin" id="dtDateJoin" fieldname="DateJoin" placeholder="mm/dd/yyyy">
                    </div>
                    <div class="right">
                        <label for="dtDateJoin">Tình trạng công việc</label>
                        <select name="Gender" id="dtDateJoin" fieldname="StateId">
                        </select>
                    </div>
                </div>
            </div>
        </div>
        <div class="dialog-footer">
            <button id="btnSave">Lưu</button>
            <button id="btnDelete" v-show="btnDeleteState">Xóa</button>
            <button id="btnCancel" @click="closeDialog">Hủy</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Dialog',
        data() {
            return {
                btnDeleteState: false
            }
        },
        methods: {
            closeDialog() {
                debugger; //eslint-disable-line no-debugger
                this.$emit('close-dialog');
            }
        }
    }
</script>

<style scoped>
    @import '../css/dialog.css';
</style>
