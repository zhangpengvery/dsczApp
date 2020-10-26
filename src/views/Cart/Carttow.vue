<!--  -->
<template>
<div class='cart'>
    <Head title="购物车" :left="left" :right="right" />
        <div class="cart-content" v-if="true">
            <ul>
                <li>
                    <div class="select">
                       <i class="iconfont icon-danxuankuang" v-if="true"></i>
                       <i class="iconfont icon-danxuankuangxuanzhong" v-else></i>
                    </div> 
                    <div class="cart-img">
                        <img src="" alt="">
                    </div>
                    <div class="cart-info">
                        <div class="cart-title"></div>
                        <div class="cart-wrap">
                            <span class="price"></span>
                            <div class="cart-num">
                                <a href="javascript:;">-</a>
                                <input type="number" value="1" >
                                <a href="Javascript:;">+</a>
                                <button class="ded iconfont icon-shanchu1"></button>
                            </div>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
        <div class="nocart" v-else>
            <div class="checkAll">
                <i class="iconfont icon-gouwuche"></i>
                <p>不选东西来个√8购物车
                    <router-link to="/home">去逛逛</router-link>
                </p>
            </div>
        </div>
        <div class="cartFooter" v-if="true">
                <div class="checkAll">
                    <i class="iconfont icon-danxuankuang" v-if="true"></i>
                    <i class="iconfont icon-danxuankuangxuanzhong" v-else></i>
                    <span>全选</span>
                </div>
                <div class="priceAll">
                    合计:
                    <span>10</span>
                </div>
                <div class="gobuy">去结算：1W</div>
            </div>
            <Footer>
</div>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';
import Footer from "@/components/Footer";
import Head from "@/components/Head";
export default {
  //import引入的组件需要注入到对象中才能使用
  components: {
    Footer,
    Head,
  },
  data() {
    //这里存放数据
    return {
      left: true,
      right: false,
    };
  },
  //监听属性 类似于data概念
  computed: {},
  //监控data中的数据变化
  watch: {},
  //方法集合
  methods: {},
};
</script>
<style>
</style>