<!-- Created By liuhuihao 2018/5/30 14:38  -->
<!-- 播放器时间显示组件 -->
<template>
    <div class="music-info">
        {{currentTimeFormat}} ' {{durationFormat}}
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';

    export default {
        name: 'musicInfo',
        computed: {
            ...mapGetters(['durationFormat', 'currentTimeFormat']),
        }
    }
</script>

<style lang="less" scoped>
    .music-info {
        color: rgba(235, 12, 238, 0.8);
        font-size: 22px;
        letter-spacing: 1px;
        z-index: -1;
        margin: 20px 0 0 0;
        pointer-events: none;
        user-select: none;
    }
</style>