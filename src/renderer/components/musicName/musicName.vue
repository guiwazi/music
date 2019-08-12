<!-- Created By liuhuihao 2018/5/25 10:38  -->
<!-- 播放器歌曲名称组件 -->
<template>
    <div class="music-name">
        {{currentMusicFileName}}
    </div>
</template>

<script>
    import {mapGetters} from 'vuex';

    export default {
        name: 'musicName',
        computed: {
            ...mapGetters([
                'currentMusicFileName'
            ]),
        }
    }
</script>

<style lang="less" scoped>
    .music-name {
        color: rgba(255, 255, 255, 0.8);
        font-size: 32px;
        letter-spacing: -1px;
        z-index: -1;
        pointer-events: none;
        user-select: none;
        -webkit-animation:music_name 10s  infinite linear reverse;
    }
@keyframes music_name
{
    0 {color:#FD175D;opacity: 1;}
    20% {color:#9C1BF7;opacity: 0.9;}
    40% {color:#2E8BFF;opacity: 1;}
    60% {color:#24F869;opacity: 0.9;}
    80% {color:#EBFB16;opacity: 1;}
    100% {color:#FF7C2B;opacity: 0.1;}
}
</style>