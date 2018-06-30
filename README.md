# jsonFormat

## json数据格式化

```
 /**
    * 说明： 
    * 参数 jsonData 为json数据，调用此页面之前先判断是否为json格式数据
    * 参数 textData 为已选择的数据
    * 参数 callback 为选择后的回调
    */

var config = {
    jsonData:  {
    "name": "testname",
    "url": "http://www.test.com",
    "page": 88,
    "isNonProfit": true,
    "address": {
        "street": "笑话大全",
        "city": "江苏苏州",
        "country": "中国"
    },
    "links": [
        {
        "name": "Google",
        "url": "http://www.google.com",
        'arr': [
            1, 2, 3
        ]
        },
        {
        "name": "Baidu",
        "url": "http://www.baidu.com"
        }
    ]
    },
    textData: 'page,address,address.city,links.*.url,links.*.arr.*',
    callback: function(res) {
    // 选择后返回的值
    console.log(res);
    }
};
```