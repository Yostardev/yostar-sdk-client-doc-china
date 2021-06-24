### 1、SDK初始化

\* 调用该接口完成SDK的初始化工作;<br/>\* 在初始化成功的情况下，才能调用SDK其他接口;<br/>
\* 调用该接口前，请先设置InitEvent监听回调，以便初始化成功后,顺利收到初始化成功的事件;


- #### 函数定义

  ```cs
    public bool Init()
  ```
<br/>

- #### 调用示例

  ```cs
      private void OnInitRespone(InitRet ret){//callback

          if (ret.R_CODE == ResultCode.OK){
              // init success,game continue
          }else{
              // init fail, do not anything
          }
      }

      YoStarSDKEvent.Instance.InitEvent += OnInitRespone;

      YoStarSDK.Instance.Init("https://audit-sdk-api.yostar.cn");
  ```

    InitRet 属性名|参数说明|备注
    ---|:--:|:--|
    R_CODE|状态码,枚举值|0:成功<br/> 其他值可查看第7章错误码表含义|
    R_MSG| 错误信息,辅助排查问题|无 |
