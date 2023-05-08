<template>
    <el-container>
        <el-main>
            <el-row justify="center">
                <el-col span="8">
                    <el-input placeholder="名称/编号" />
                </el-col>
                <el-col span="auto">
                    <el-button type="primary">search</el-button>
                </el-col>
            </el-row>
            <el-row>
                <el-button>新增</el-button>
                <el-button>删除</el-button>
            </el-row>
            <el-table :data="tableData ">
                <el-table-column type="selection" />
                <el-table-column label="编号" prop="id" align="center"/>
                <el-table-column label="座位总数" prop="total" align="center"/>
                <el-table-column label="预约情况" prop="state" align="center"/>
                <el-table-column label="操作" align="center">
                    <el-button>详情</el-button>
                    <el-button>删除</el-button>
                </el-table-column>
            </el-table>
        </el-main>
    </el-container>
</template>
<script>
export default {
    name: 'RoomInfo',
    data() {
        return {
            tableData: [
                {
                    id: "111",
                    total: 50,
                    state: "空闲"
                },
                {
                    id: "111",
                    total: 50,
                    state: "空闲"
                },
                {
                    id: "111",
                    total: 50,
                    state: "空闲"
                }
            ]
        }
    }
}
</script>
<style scoped></style>