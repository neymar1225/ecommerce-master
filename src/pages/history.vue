<template>
  <div class="main">
    <div class="contain1"></div>
    <div class="contain2">
      <div class="title_name">
        <div class="text">
          <em></em> 
          我的足迹
          <b>MY TRACKS</b>
        </div>
        <div class="btn">
          <button @click="clearHistory">清空历史记录</button>
        </div>
      </div>
      <hr>
      <div class="items">
        <ul style="list-style: none;">
          <li v-for="product in footprints" :key="product.id">
            <div class="item_child">
              <div class="child_img">
            <img :src="require(`@/assets/img/${product.image}`)" alt="Product Image">
              </div>
              <div class="child_int">
              <a href="">{{ product.name }}</a>
              <span>价格: {{ product.price }}</span>
              <p>查看时间: {{ product.viewedAt | formatDate }}</p>
            </div>
          </div>
          </li>
        </ul>
      </div>
    </div>
    <div class="contain1"></div>
  </div>
</template>

<script>
import myHead from '@/components/myHead.vue';

export default {
  components: { myHead },
  name: "history",
  data() {
    return {
      footprints: [
        { id: 1, name: '抽绳垃圾袋抽绳手提式自动收口垃圾袋家用45*50cm抽绳款', image: '垃圾袋.jpg', price: '￥5.10', viewedAt: new Date() },
        { id: 2, name: '爱因斯坦的脑子。付款后自动长到你大脑上。买过的都说好用。', image: '脑子.jpg', price: '￥0.1', viewedAt: new Date() },
        { id: 3, name: '创意恶搞奖杯你真牛杯玩偶鲨杯牛芒毛绒玩具抱枕牛啤公仔优趣优品', image: '牛.jpg', price: '￥28.5', viewedAt: new Date() },
        { id: 4, name: '网红重力3D迷你小手枪1911幼崽大学生解压萝卜枪儿童玩具不可发射', image: '刀.jpg', price: '￥18.5', }
        // 添加更多足迹商品
      ],
      showFootprints: true  // 控制是否显示足迹信息的状态
    };
  },
  methods: {
    clearHistory() {
      this.footprints = [];
      this.showFootprints = false;
    }
  },
  filters: {
    formatDate(date) {
      // 自定义日期格式化过滤器
      const options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: 'numeric', minute: 'numeric' };
      return new Intl.DateTimeFormat('en-US', options).format(date);
    }
  }
};
</script>


<style lang="scss" scoped>
.main{
  margin-top: 50px;
  display: flex;
  width: 100%;
}
.contain1{
  width: 20%;
}
.contain2{
  text-align: center;
  width: 60%;
  display: flex;
  border: groove 5px rgb(115, 113, 113,0.5);
  border-radius: 30px;
  flex-direction: column;
  flex-wrap: nowrap;
}
.title_name{
  display: flex;
  padding: 5px;
  border-bottom: rgb(148, 150, 150) solid;
  border-right: rgb(148, 150, 150) solid;

  border-radius: 15px;
  margin-top: 30px;
  margin-left: 20px;
  margin-right: 20px;
  justify-content: space-between;
}
.text{
  text-align: center;
    display: flex;
    align-items: center;
    font-size: 18px;
    color: #d68c8c;
}
em{
  margin-left: 2px;
  border: rgb(223, 92, 92) solid 3px;
  border-radius: 50px;
  margin-right: 10px;
  margin-left: 5px;
}

hr{
  width:2px;
  border-width:0;
  background-color:#000;
  margin-left: 10px;
}
.btn{
  border-radius: 15px;
  background: rgb(163, 220, 127);
}
.btn button{
  border: none;
  border-radius: 15px;
  background-color: rgb(163, 220, 127);
}
@media (max-width: 768px) {
  .contain2 {
    width: 100%; /* 或者适当调整宽度 */
  }

  .item_child img {
    height: 80px; /* 调整图片尺寸 */
    width: 120px;
  }
}

.items{
  margin-left: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  flex-wrap: nowrap;
  width: 100%;
}
.item_child{
  display: flex;
    width: 100%;
    margin-bottom: 20px;
}
.item_child img{
  border-radius: 15px;
  height: 120px;
  width: 160px;
}
.child_int{
  margin-left: 30px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
a{
  text-decoration:none;
  color: #000;
}
</style>

