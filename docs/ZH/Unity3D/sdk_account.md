### 2、账号登录
<span id = "login"/>

\* 参考下面的调用示例，请先设置LoginEvent监听回调，以便登录成功后,顺利收到登录成功的事件;


- #### 函数定义

  ```cs
    public void Login()
  ```

- #### 调用示例
    ```cs
    private void OnLoginRespone(LoginRet ret){ //callBack

      if (ret.R_CODE == ResultCode.OK){
          // login success,game continue
      }else {
         // login fail,do not anything
      }
    }

    YoStarSDKEvent.Instance.LoginEvent += OnLoginRespone;
    YoStarSDK.Instance.Login();
    ```

    | LoginRet    | 参数说明 | 备注 |
    | -------------- | ------ | ------ |
    | R_CODE   | ResultCode(枚举) |错误码 |
    | R_MSG     | 错误信息,辅助排查问题 | 无 |
    | LOGIN_UID   | SDK登陆成功之后返回UID | 无 |
    | MOBILE_PHONE | 绑定的手机号 | 无 |
    | ID_CARD | 绑定的身份证号 | 无 |
    | SURPLUS_DURATION | 防沉迷剩余时间 | 单位/秒 |





