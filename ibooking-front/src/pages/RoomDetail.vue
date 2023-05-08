<template>
    <el-container>
        <el-main>
            <el-row>
                <el-text size="large" type="info">Room 001</el-text>
            </el-row>

            <el-row>
                <el-col span="4">
                    <div class="seat-state available"></div>
                </el-col>
            </el-row>
        </el-main>
    </el-container>
</template>
<script>
export default {
    name: "RoomDetail"
}
</script>
<style scoped>
.seat-state {
    /* width: 100%;
    height: 0;
    padding-bottom: 100%; */
    width: 100px;
    height: 100px;
}

.seat-state.available {
    background: green;
}
</style>