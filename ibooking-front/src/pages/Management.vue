<template>
    <div class="background">
        <div class="container">
            <div class="toolbar">
                <div class="logo">
                    <img src="@/assets/standard_logo.png" />
                    <!-- <div class="line"></div> -->

                </div>
                <div>
                    <LoginInfo></LoginInfo>
                    <!-- <div class="login">登录</div> -->
                </div>
            </div>
            <div class="title">自习室管理系统</div>

            <el-container class="main">
                <el-aside style="width: auto;">
                    <el-menu default-active="1" class="el-menu-vertical-demo" style="height: 100%;">
                        <el-menu-item class="menu-item" index="1">
                            个人信息
                        </el-menu-item>
                        <el-menu-item class="menu-item" index="2">
                            自习室
                        </el-menu-item>
                        <el-menu-item class="menu-item" index="3">
                            预约
                        </el-menu-item>
                        <el-menu-item class="menu-item" index="4">
                            预约信息
                        </el-menu-item>
                    </el-menu>
                </el-aside>
                <!-- <PersonalInfo></PersonalInfo> -->
                <!-- <RoomInfo></RoomInfo> -->
                <!-- <BookingInfo></BookingInfo> -->
                <RoomDetail></RoomDetail>
            </el-container>

            <!-- <div class="main"> -->

            <!-- <div >

                </div>
                <PersonalInfo></PersonalInfo> -->
            <!-- <div class="buttonbar">
                    <button>新增自习室</button>
                    <button>新增自习室</button>
                    <button>新增自习室</button>
                </div> -->

            <!-- </div> -->
        </div>
    </div>
</template>
<script>
import LoginInfo from "@/components/LoginInfo.vue";
import RoomInfo from "./RoomInfo.vue";
import PersonalInfo from "./PersonalInfo.vue";
import BookingInfo from "./BookingInfo.vue";
import RoomDetail from "./RoomDetail.vue"
export default {
    name: 'Management',
    components: {
        LoginInfo,
        PersonalInfo,
        RoomInfo,
        BookingInfo,
        RoomDetail
    }
}
</script>
<style scoped>
.background {
    background: url("~@/assets/bg.jpg") 0% 0% / 100% no-repeat;
    height: 100%;
}

.container {
    width: 1061px;
    height: 100%;
    margin: 0 auto;
}

.toolbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 68px;
}

.logo img {
    max-height: 48px;
}

.login {
    width: 78px;
    height: 32px;
    background: #fff;
    border-radius: 4px;
    line-height: 32px;
    text-align: center;
    font-size: 14px;
    font-weight: 500;
    cursor: pointer;
    color: #2E8CF0;
}

.title {
    font-size: 36px;
    line-height: 1.5;
    display: block;
    margin: 12px 0;
    font-weight: 700;
    color: #fff;
}

.main {
    background: #fff;
    -webkit-box-shadow: 0 4px 20px 0 rgba(226, 234, 242, .5);
    box-shadow: 0 4px 20px 0 rgba(226, 234, 242, .5);
    border-radius: 8px;
    overflow: hidden;
    height: calc(100% - 194px - 12px);
}

.menu-item {
    display: block;
    text-align: center;
}

.buttonbar {
    display: flex;
    justify-content: end;
}

.buttonbar button {
    font-size: 12px;
    color: #2E8CF0;
    cursor: pointer;
    padding: 8px 12px;
    border: #2E8CF0 solid 1px;
    border-radius: 4px;
    background: #fff;
}

.buttonbar button+button {
    margin-left: 10px;
}
</style>