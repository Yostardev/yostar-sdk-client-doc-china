### 1、发起支付
\* 该接口需账户登录成功后才能调用;<br/>\* 调用该接口可实现游戏道具的购买;<br/>\* 调用该接口前,务必先设置PayEvent监听回调，以便支付操作后,顺利收到操作结果的事件;


- #### 未成年人氪金限制:
  年龄|氪金限制|备注|
  ---|:--:|:--:|
  小于12周岁|不可氪金|无|
  12 ～ 16|单次不超过50，每月累计不超过200|无|
  16 ～ 18|单次不超过100，每月累计不超过400|无|

 </br>

- #### 测试商品信息:
  商品ID|价格|备注|
  ---|:--:|--:|
  1|¥9.9|无|
  2|¥19.9|无|
  3|¥98.9|无|
  4|¥198.9|无|
  5|¥598.9|无|

 </br>

- #### 函数定义
    ```cs
    public ResultCode Pay(int productId)
    ```

    入参名称|入参说明|备注
    ---|:--:|:--|
    productId|需要支付的产品Id|无|

- #### 调用示例

    ```cs
    private void OnPayRespone(PayRet ret){

       if (ret.R_CODE == ResultCode.OK){

            // pay success
        }else{

           // pay fail
        }
    }

    YoStarSDKEvent.Instance.PayEvent += OnPayRespone;
    YoStarSDK.Instance.Pay(2);
    ```

    PayRet 属性名|类型|参数说明|备注
    ---|:--:|:--|:--|
    R_CODE|ResultCode(枚举)|状态码,枚举值|0:成功<br/> 其他值可查看错误表含义|
    R_MSG|string| 错误信息,辅助排查问题|无 |
    ORDER_ID|int| 悠星订单号|无 |
    PRODUCT_ID|int| 购买的产品ID|无 |

