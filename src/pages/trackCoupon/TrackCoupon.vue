<template>
  <div>
    <van-row  v-for="(item, index) in list" :key="index" gutter="10" class="bg-light mx-0 border-bottom py-1" type="flex" align="center">
      <van-col span="8" class="text-center">
        <img :src="item.thumb" alt="" style="width: 85%;">
      </van-col>
      <van-col span="8" class="text-left">
        <p class="mb-0">{{item.title}}</p>
        <p class="van-ellipsis mb-0">{{item.rule}}</p>
        <p class="mb-0 text-danger font-weight-bold" style="font-size: 14px;">￥{{item.bills}}</p>
      </van-col>
      <van-col span="8">
        <p class="mb-0">
          <van-stepper class="mt-1" v-model="item.value" />
        </p>
        <p class="mb-0 mt-1 text-center">
          <van-button type="info" size="small" @click="buyNow(item)">立即购买</van-button>
        </p>
      </van-col>
    </van-row>
  </div>
</template>

<script>
  export default {
    name: "saiDaoQuan",
    data () {
      return {
        list: []
      }
    },
      mounted () {
        this.myCouponList()
      },
    methods: {
        // 立即购买
        buyNow (item) {
            this.$router.push({path: `/firmorder?cartIds=${item.id}`, query: {item: JSON.stringify(item)}})
        },
        // 获取赛道券列表
        myCouponList () {
            this.$api.myCoupon({}, res => {
                if (res.status) {
                    this.list = res.data
                }
            })
        },
    }
  }
</script>

<style scoped>
  .van-card__price{
    font-size: 20px;
  }
</style>
