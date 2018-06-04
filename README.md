# shell-house
#### 贝壳新房
* 微信小程序编写
* 前后端数据交互完成页面渲染
```
getMainCard: function(){
    const that = this;
    wx.request({
      url:"http://47.93.220.17/Home/Bk/xinfang",
      method:"get",
      datatype:"json",
      success: function (res) { 
          that.setData({
            mainCard:res.data
          });
      },
    }) 
  },
  getMainList: function(){
    const that = this;
    wx.request({
      url: "http://47.93.220.17/Home/Bk/getListsByType",
      method: "get",
      datatype: "json",
      success: function (res) {
        that.setData({
          mainList: res.data
        });
      },
    }) 
  },
  tapName: function (event) {
    console.log(event)
  }
```
