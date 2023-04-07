<template>
    <div class="room-item">
        <div class="more">
            <div class="icon" ref="more" @click="clickMore">···</div>
            <transition name="fade">
                <div class="panel" v-if="moreShow">
                    <div class="panel-item">删除自习室</div>
                    <div class="panel-item">管理自习室</div>
                </div>
            </transition>

        </div>
        <div class="room-id">A100</div>
        <div class="seat">
            <div class="label">
                <div>已预约座位：</div>
                <div>可预约座位：</div>
                <div>故障座位：</div>
            </div>
            <div class="count">
                <div>0/50</div>
                <div>50/50</div>
                <div>0</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'RoomItem',
    data() {
        return {
            moreShow: false,
        }
    },
    methods: {
        clickMore() {

            this.moreShow = true;
            window.addEventListener("click", this.closeMore);
        },
        closeMore(event) {
            if (event.target != this.$refs.more) {
                this.moreShow = false;
                window.removeEventListener("click", this.closeMore);
            }
        }
    }
}
</script>
<style scoped>
.room-item {
    width: 100%;
    box-sizing: border-box;
    font-size: 14px;
    border-radius: 4px;
    border: 1px solid rgba(187, 187, 187, .5);
    box-shadow: 0 4px 20px 0 rgba(226, 234, 242, .5);
    padding: 18px 28px;
    position: relative;
}

.more {
    position: absolute;
    right: 6px;
    top: 3px;
}

.more .icon {
    width: 20px;
    height: 20px;
    font-size: 22px;
    color: #666;
    border-radius: 50%;
    cursor: pointer;
    text-align: center;
}

.more .icon:hover {
    background: rgba(0, 0, 0, 0.03);
}

.more .panel {
    position: absolute;
    right: 0;
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 3px 4px #bbb;
}

.more .panel-item {
    padding: 6px 12px;
    color: #2E8CF0;
    white-space: nowrap;
    cursor: pointer;
}

.more .panel-item:hover {
    background: rgba(0, 0, 0, 0.03);
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

.room-id {
    font-size: 18px;
    font-weight: 700;
    color: #666;
    text-align: center;
    margin-bottom: 10px;
}

.seat {
    display: flex;
    justify-content: space-between;
}

.seat .label {
    text-align: justify;
    text-align-last: justify;
    color: #666;
}

.seat .count {
    text-align: center;
}</style>