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

    | resultMap属性 |类型| 参数说明 | 备注 |
    | ---- | ---- | ------ | ------ |
    | LOGIN_UID | int |账号ID | 无 |
    | MOBILE_PHONE | string | 绑定的手机号 | 无 |
    | ID_CARD | string |绑定的身份证号 | 无 |
    | SURPLUS_DURATION | int | 防沉迷剩余时间 | 单位/秒 |






