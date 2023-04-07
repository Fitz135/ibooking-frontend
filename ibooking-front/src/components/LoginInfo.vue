<template>
    <div class="user" @mouseenter="mouseenter" @mouseleave="mouseleave">
        <div class="user-icon"></div>
        <div class="name">陆天一</div>
        <div class="arrow"></div>
        <transition name="fade">
            <div class="panel-container" v-if="panelShow">
                <div class="panel">
                    <div class="panel-item">安全退出</div>
                    <div class="panel-item">安全退出</div>
                    <div class="panel-item">安全退出</div>
                </div>
            </div>
        </transition>
    </div>
</template>
<script>
export default {
    name: 'LoginInfo',
    data() {
        return {
            panelShow: false
        }
    },
    methods: {
        mouseenter() {
            this.panelShow = true;
        },
        mouseleave() {
            this.panelShow = false;
        }
    }
}
</script>
<style scoped>
.container {
    position: relative;
    display: inline-block;
}

.user {
    display: flex;
    align-items: center;
    cursor: pointer;
    position: relative;

}

.user-icon {
    width: 18px;
    height: 18px;
    box-sizing: border-box;
    border: #fff solid 2px;
    border-radius: 50%;
    overflow: hidden;
    position: relative;
}

.user-icon::before {
    content: "";
    width: 7.5px;
    height: 7.5px;
    box-sizing: border-box;
    border: #fff solid 2px;
    border-radius: 50%;
    position: absolute;
    left: 50%;
    top: 45%;
    transform: translate(-50%, -50%);
}

.user-icon::after {
    content: "";
    width: 16px;
    height: 16px;
    box-sizing: border-box;
    border: #fff solid 2px;
    border-radius: 50%;
    position: absolute;
    left: 50%;
    top: 110%;
    transform: translate(-50%, -50%);
}

.name {
    display: inline-block;
    max-width: 72px;
    min-width: 28px;
    margin-left: 8px;
    color: #fff;
    font-size: 16px;
}

.arrow {
    margin-left: .8em;
    border-left: 7px solid transparent;
    border-right: 7px solid transparent;
    border-bottom: 8px solid transparent;
    border-top: 8px solid #fff;
    display: inline-block;
    transform: translateY(40%);
    transform-origin: 50% 60%;
    -webkit-transition: -webkit-rotate .2s;
    transition: rotate .2s;
}

.user:hover .arrow {
    rotate: 180deg;
}

.panel-container {
    position: absolute;
    right: 0;
    bottom: 0;
    transform: translateY(100%);
}

.panel {
    margin-top: 16px;
    border-radius: 4px;
    background: #fff;
    box-shadow: 0 3px 4px #bbb;
}

.panel-item {
    font-size: 14px;
    padding: 14px 28px;
    color: #000;
    white-space: nowrap;
    cursor: pointer;
}

.panel-item:hover {
    background: rgba(0, 0, 0, 0.03);
}

.panel-item+.panel-item {
    border-top: rgba(0, 0, 0, 0.1) solid 1px;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
    transition: all 0.3s;
}

.fade-enter-to,
.fade-leave-from {
    opacity: 1;
}
</style>