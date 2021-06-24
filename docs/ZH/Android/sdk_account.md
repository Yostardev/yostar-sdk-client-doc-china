### 1、账号登录
<span id = "login"/>

\* 参考下面的调用示例，请先设置AiriSDK.setCallBack监听回调，以便登录成功后,顺利收到登录成功的事件;


- #### 函数定义

  ``` java
  public static void login(Activity activity)
  ```

- #### 调用示例

    ``` java
    AiriSDK.login(MainActivity.this);
    ```
- #### 回调示例

    ``` java
    {"LOGIN_PLATFORM":0,"METHOD":"OnLoginNotify","LOGIN_UID":"40119188699623424","R_MSG":" success ","R_CODE":0,"MOBILE_PHONE": "","ID_CARD": "","SURPLUS_DURATION":0}
    ```

    | resultMap属性    | 参数说明 | 备注 |
        | ---- | ---- | ------ |
        | R_CODE | 状态码,枚举值 | 0:成功<br/>其他值可查看错误表含义 |
        | R_MSG | 错误信息,辅助排查问题 | 无  |
        | LOGIN_UID | 账号ID | 无 |
        | MOBILE_PHONE | 绑定的手机号 | 无 |
        | ID_CARD | 绑定的身份证号 | 无 |
        | SURPLUS_DURATION | 防沉迷剩余时间 | 单位/秒 |






