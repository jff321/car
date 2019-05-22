<template>
    <div class="indexgrids">
        <yd-grids-group rows="4">
            <yd-grids-item link="/track" >
                <img slot="icon" src="../../static/image/track.png">
                <span slot="text">赛道</span>
            </yd-grids-item>
            <yd-grids-item link="/trackCoupon" >
                <img slot="icon" src="../../static/image/quan.png">
                <span slot="text">赛道券</span>
            </yd-grids-item>
            <yd-grids-item link="/allorder" >
                <img slot="icon" src="../../static/image/activity.png">
                <span slot="text">活动</span>
            </yd-grids-item>
            <yd-grids-item link="/collect" >
                <img slot="icon" src="../../static/image/yuyue.png">
                <span slot="text">预约</span>
            </yd-grids-item>
        </yd-grids-group>
        <yd-grids-group rows="4">
            <yd-grids-item link="/classify" >
                <img slot="icon" src="../../static/image/group10.png">
                <span slot="text">全部分类</span>
            </yd-grids-item>
            <yd-grids-item link="/goodslist?hot=1" >
                <img slot="icon" src="../../static/image/group11.png">
                <span slot="text">热卖商品</span>
            </yd-grids-item>
            <yd-grids-item link="/allorder" >
                <img slot="icon" src="../../static/image/group14.png">
                <span slot="text">我的订单</span>
            </yd-grids-item>
            <yd-grids-item link="/collect" >
                <img slot="icon" src="../../static/image/group15.png">
                <span slot="text">我的收藏</span>
            </yd-grids-item>
        </yd-grids-group>
    </div>
</template>

<script type="text/babel">
export default {
}
</script>
<style type="text/css">
</style>
