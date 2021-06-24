### 1、发起支付
\* 该接口需账户登录成功后才能调用;<br/>\* 调用该接口可实现游戏道具的购买;<br/>\* 调用该接口前,务必先设置PayEvent监听回调，以便支付操作后,顺利收到操作结果的事件;

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

    PayRet 属性名|参数说明|备注
    ---|:--:|:--|
    R_CODE|状态码,枚举值|0:成功<br/> 其他值可查看错误表含义|
    R_MSG| 错误信息,辅助排查问题|无 |
    LOGIN_UID| 用户ID|无 |
    ORDER_ID| 悠星订单号|无 |
    PRODUCT_ID| 购买的产品ID|无 |

