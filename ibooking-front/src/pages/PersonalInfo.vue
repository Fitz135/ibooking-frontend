<template>
    <el-container>
        <el-main>
            <el-row style="height: 100%;" justify="center" align="middle">
                <el-form style="width: 33%">
                    <el-form-item label="学号">
                        <el-input />
                    </el-form-item>
                    <el-form-item label="姓名">
                        <el-input />
                    </el-form-item>
                    <el-form-item label="电话">
                        <el-input />
                    </el-form-item>
                    <el-form-item label="邮箱">
                        <el-input />
                    </el-form-item>
                </el-form>
            </el-row>
        </el-main>
        <el-footer>
            <el-row justify="end">
                <el-button type="primary">提交</el-button>
                <el-button>重置</el-button>
            </el-row>
        </el-footer>
    </el-container>
</template>
<script>
export default {
    name: 'PersonalInfo',
}
</script>
<style scoped></style>