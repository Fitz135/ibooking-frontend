<template>
    <el-container>
        <el-main>
            <el-row>
                <el-text size="large" type="info">当前预约</el-text>
            </el-row>
            <el-table>
                <el-table-column label="自习室" align="center"/>
                <el-table-column label="座位" align="center"/>
                <el-table-column label="预约时间" align="center"/>
                <el-table-column label="状态" align="center"/>
                <el-table-column label="操作" align="center">
                    <el-button>签到</el-button>
                    <el-button>取消</el-button>
                </el-table-column>
            </el-table>

            <el-row style="margin-top: 24px;">
                <el-text size="large" type="info">历史预约</el-text>
            </el-row>
            <el-table>
                <el-table-column label="自习室" align="center"/>
                <el-table-column label="座位" align="center"/>
                <el-table-column label="预约时间" align="center"/>
                <el-table-column label="状态" align="center"/>
            </el-table>
        </el-main>
    </el-container>
</template>
<script>
export default {
    name: "BookingInfo"
}
</script>