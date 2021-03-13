# 安装使用 #

```
npm i vue-stars-rating -S  OR yarn vue-stars-rating
 
```

# 说明 #

>改自 原创 JonathanDn 的开源组件 


# 功能 #

>1、点击评分 Click score
>2、静态展示 Static display



| parmas |value | remarks |
|--|--|--|
|clickChange|Boolean| 默认 false, 是否可以点击；false为不可以点击 |
|config|Object|具体查看下面示例讲解|
|stroke|String|描边颜色，边框|
|itemclick|Fn|点击事件回调名称 @itemclick="itemclick"  该函数有三个参数（num=评分，i=star下标，event=原型）|



# 完整用法 #

```
 <template>  
    <div>
      <stars-rating clickChange  stroke="#ECB871" v-bind="config" @itemclick="itemclick"></stars-rating>  
    </div>
  </template>
```

```
 data() {
      return {
        config: {
          rating: 4.9,//设置评分
          isIndicatorActive: false,//是否显示测试数据到页面上
          starStyle: {
            fullStarColor: "#ECB871",//填充颜色
            emptyStarColor: "rgba(0,0,0,0)",//背景填充颜色
            starWidth: 100,//宽度
            starHeight: 100//高度
          }
        }
      };
 },

```

```
    methods: {
      itemclick(num) {       
        this.$set(this.config,"rating", num); 
      }
    },


```