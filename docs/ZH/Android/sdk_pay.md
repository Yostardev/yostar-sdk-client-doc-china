### 1、发起支付
\* 该接口需账户登录成功后才能调用;<br/>\* 调用该接口可实现游戏道具的购买;<br/>\* 调用该接口前,务必先设置AiriSDK.setCallBack监听回调，以便支付操作后,顺利收到操作结果的事件;

- #### 函数定义
    ``` java
    public static void pay(Activity activity, String productId)
    ```

    入参名称|类型|入参说明|备注
    ---|:--:|:--|:--|
    productId|string|需要支付的产品Id|无|

- #### 调用示例

    ``` java
    AiriSDK.pay(MainActivity.this, 1);
    ```
- #### 回调示例
    ``` java
    {"LOGIN_UID":123,"PRODUCT_ID":2,"ORDER_ID":1250504353048453120,"METHOD":"OnPayNotify","R_MSG":" success ","R_CODE":0}
    ```
  
    resultMap 属性名|类型|参数说明|备注
    ---|:--:|:--|:--|
    ORDER_ID|string| 悠星订单号|无 |
    PRODUCT_ID|string| 购买的产品ID|无 |
