### 1、SDK初始化

\* 调用该接口完成SDK的初始化工作;<br/>
\* 在初始化成功的情况下，才能调用SDK其他接口;<br/>
\* 调用该接口前，请先设置AiriSDK.setCallBack监听回调，以便初始化成功后,顺利收到初始化成功的事件;


- #### 函数定义

  ``` java
  public static void init(Activity activity, String sdkUrl)
  ```

    入参名称|类型|入参说明|备注
    ---|:--:|:--|:--|
    sdkUrl|string|SDK服务器地址|无|

<br/>

- #### 调用示例

  ``` java
  AiriSDK.init(MainActivity.this, "https://xxxxx.arknights.com");
  ```
- #### 回调示例
  ``` java
    {"METHOD":"OnInitNotify","R_MSG":"success","R_CODE":0}
  ```
  