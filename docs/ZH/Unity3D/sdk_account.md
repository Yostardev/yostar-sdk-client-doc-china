### 1、账号登录
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

    private void OnLogoutResponse(LogoutRet ret){

        // logout success,game continue
    }
    YoStarSDKEvent.Instance.logoutEvent += OnLogoutResponse;


    YoStarSDK.Instance.Login();
    ```

    | LoginRet    |类型| 参数说明 | 备注 |
    | -------------- | ------ | ------ | ------ |
    | R_CODE   | ResultCode(枚举) |错误码 |
    | R_MSG     |string| 错误信息,辅助排查问题 | 无 |
    | LOGIN_UID   |int| SDK登陆成功之后返回UID | 无 |
    | MOBILE_PHONE |string| 绑定的手机号 | 无 |





