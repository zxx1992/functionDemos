<!--
 * @Author: zhengxiaoxiao
 * @Date: 2020-07-02 11:37:49
 * @Description: 评分组件
--> 
<template>
<div>
  <div class="rate-content">
    <input type="radio" name="rate">
    <input type="radio" name="rate">
    <input type="radio" name="rate">
    <input type="radio" name="rate">
    <input type="radio" name="rate">
  </div>
  <a href="https://coding.zhangbing.site/">组件代码路径</a>
</div>
</template>
<style>
/* 注意： 这里加scoped, css var()函数不起作用 */
/* 去掉默认样式 */
input {
  -webkit-appearance: none;
  border: none;
  outline: none;
  cursor: pointer;
}

:root {
  /*高亮颜色*/
  --main: #ffa822;
  /*默认颜色*/
  --basic: #999;
}

.rate-content input[name="rate"] {
  font-family: "iconfont";
  /*之前引入的iconfont字体*/
  font-size: 30px;
  padding-right: 10px;
}

.rate-content input[name="rate"]::after {
  content: "\e7cb";
  color: var(--basic);
  /*加点颜色过渡效果*/
  transition: color 0.4s ease;
}

/* 实现选中单个星星 */
/* 高亮的星星 */
input[name="rate"]:checked::after,
input[name="rate"]:checked ~ input[name="rate"]::after {
  /*实现连同兄弟元素一起高亮*/
  content: "\e7bd";
  color: var(--main);
}

/* 把input反向排列 */
.rate-content {
  display: flex;
  flex-flow: row-reverse;
  justify-content: center;
}

input[name="rate"] {
  margin-right: 10px;
  transition: transform 0.2s ease;
}

input[name="rate"]:checked,
input[name="rate"]:hover::after {
  content: "\e7bd";
  color: var(--main);
}

/* 兄弟元素一起高亮 */
input[name="rate"]:hover ~ input[name="rate"]::after {
  content: "\e7bd";
  color: var(--main);
}

input[name="rate"]:checked,
input[name="rate"]:hover {
  transform: scale(1.2);
}
</style>