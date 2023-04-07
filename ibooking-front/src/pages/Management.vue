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
            <div class="searchbar">
                <input />
                <button>搜索</button>
            </div>
            <div class="search-history">
                <span>最近搜索：</span>
                <span class="item">入学复查</span>
            </div>
            <div class="main">
                <div class="buttonbar">
                    <button>新增自习室</button>
                    <button>新增自习室</button>
                    <button>新增自习室</button>
                </div>
                <div class="roomlist">
                    <RoomItem v-for="i in 10" :key="i"></RoomItem>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import RoomItem from "@/components/RoomItem.vue"
import LoginInfo from "@/components/LoginInfo.vue"
export default {
    name: 'Management',
    components: {
        RoomItem,
        LoginInfo
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

/* .line {
    width: 1px;
    height: 26px;
    background: #e6e6f2;
    opacity: .4;
    display: inline-block;
} */


.title {
    font-size: 36px;
    line-height: 1.5;
    display: block;
    margin: 12px 0;
    font-weight: 700;
    color: #fff;
}

.searchbar {
    width: 585px;
    height: 50px;
    border-radius: 4px;
    box-sizing: border-box;
    background: #fff;
    display: flex;
    justify-content: end;
}

.searchbar input {
    display: inline-block;
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    vertical-align: middle;
    text-overflow: ellipsis;
    max-width: 90%;
    padding: 0;
    padding-left: 12px;
    font-size: 20px;
    color: #000;
    border-radius: 4px 0 0 4px;
}

.searchbar button {
    width: 120px;
    height: 100%;
    cursor: pointer;
    padding: 0;
    border: none;
    border-radius: 0 4px 4px 0;
    font-size: 20px;
    color: #fff;
    background: #2E8CF0;
}

.search-history {
    color: #fff;
    font-size: 16px;
    margin: 10px 0;
}

.search-history .item {
    cursor: pointer;
    margin-right: 20px;
    max-width: 136px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.search-history .item:hover {
    text-decoration: underline;
}

.main {
    background: #fff;
    -webkit-box-shadow: 0 4px 20px 0 rgba(226, 234, 242, .5);
    box-shadow: 0 4px 20px 0 rgba(226, 234, 242, .5);
    border-radius: 8px;
    padding: 24px 40px;
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

.roomlist {
    display: grid;
    grid-template-columns: repeat(4, auto);
    row-gap: 24px;
    column-gap: 60px;
    margin-top: 24px;
}

.roomlist .room-item {
    place-self: center;
}
</style>