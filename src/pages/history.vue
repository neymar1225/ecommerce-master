<template>
  <div class="main">
    <div class="contain1">
       
    </div>
    <div class="contain2">
      <div class="title_name">
        <div class="text">
          <em></em>
        我的足迹
        <b>MY TRACKS</b></div>
        <div class="btn">
          <button>清空历史记录</button>
        </div>
      </div>
      <hr>
      <div class="items">
        <div class="item_child">
          <div class="child_img">
            <img src="../assets/img/1.png" alt="">
          </div>
          <div class="child_int">
            <a href="">标题</a>
            <span>价钱</span>
          </div>
        </div>
        <div class="item_child">
          <div class="child_img">
            <img src="../assets/img/1.png" alt="">
          </div>
          <div class="child_int">
            <a href="">标题</a>
            <span>价钱</span>
          </div>
        </div>
        <div class="item_child">
          <div class="child_img">
            <img src="../assets/img/1.png" alt="">
          </div>
          <div class="child_int">
            <a href="">标题</a>
            <span>价钱</span>
          </div>
        </div>
        <div class="item_child">
          <div class="child_img">
            <img src="../assets/img/1.png" alt="">
          </div>
          <div class="child_int">
            <a href="">标题</a>
            <span>价钱</span>
          </div>
        </div>
      </div>
    </div>
    <div class="contain1">
      
    </div>
  </div>
</template>
<script>
import myHead from '@/components/myHead.vue';
  export default {
    components:{myHead,},
    name:"history",
  }
</script>

<style lang="scss" scoped>
.main{
  margin-top: 50px;
  display: flex;
  width: 100%;
  height: 100%;
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
b{

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
  justify-content: space-between;
  align-items: center;
}
</style>

