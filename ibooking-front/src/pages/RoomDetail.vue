<template>
    <el-container>
        <el-header style="height: auto; padding: 20px 20px 0;">
            <el-text size="large" type="info">Room 001</el-text>
        </el-header>
        <el-main>
            <el-scrollbar>
                <div style="margin-right: 20px;">
                    <el-row v-for="i in 5" :key="i" :gutter="40" style="margin-bottom: 20px;" justify="space-between">
                        <el-col v-for="j in 6" :key="j" :span="3">
                            <el-popover trigger="click" placement="right">
                                <template #reference>
                                    <div class="seat-state available"></div>
                                </template>
                                <div>
                                    <el-row>
                                        <el-text size="large">预约时间</el-text>
                                    </el-row>
                                    <el-row>
                                        <el-text size="large">预约学生</el-text>
                                    </el-row>
                                    <el-row>
                                        <el-col :span="12">
                                            <el-button>删除</el-button>
                                        </el-col>
                                        <el-col :span="12">
                                            <el-button>改状态</el-button>
                                        </el-col>
                                    </el-row>
                                </div>
                            </el-popover>
                        </el-col>
                    </el-row>
                </div>
            </el-scrollbar>
        </el-main>
        <el-footer style="height: auto; padding-bottom: 20px;">
            <el-row :gutter="15" justify="end" align="middle">
                <el-col :span="1">
                    <div class="seat-state booked"></div>
                </el-col>
                <el-col span="auto">已选</el-col>
                <el-col :span="1">
                    <div class="seat-state available"></div>
                </el-col>
                <el-col span="auto">空闲</el-col>
                <el-col :span="1">
                    <div class="seat-state disabled"></div>
                </el-col>
                <el-col span="auto">不可用</el-col>
            </el-row>
        </el-footer>
    </el-container>
</template>
<script>
export default {
    name: "RoomDetail"
}
</script>
<style scoped>
.seat-state {
    width: 100%;
    height: 0;
    padding-bottom: 100%;
    display: inline-block;
}

.seat-state.booked {
    background: #F56C6C;
}

.seat-state.available {
    background: #67C23A;
}

.seat-state.disabled {
    background: #909399;
}
</style>