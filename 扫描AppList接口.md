

- 接口加密

  AES/CBC/PKCS5Padding

- 查询扫描安装列表任务

  请求：

  ```json
  {
      "path":"/scan_pkg",
      "body":{
          "app_id":"",
          "sdk_ver":"",
          "pkg":"",
          "ver":"",
          "signature_sha1":"",
          "os":0,
          "osv":"",
          "brand":"",
          "model":"",
          "imei":"",
          "oaid":"",
          "android_id":""
      }
  }
  ```

  响应:

  ```json
  {
      "code":0,
      "msg":"",
      "data":{
          "full_scan": false,	// 全量扫描
          "report_new": true,	// 是否上报新安装的包
          "wl": [	// 白名单
              "a.b.c",
              "d.e.f"
          ],
          "bl":{	// 黑名单：不上传这些包
              "a.a.a"
          }
      }
  }
  ```

- 上报安装列表

  请求:

  ```json
  {
      "path":"/upload_pkg",
      "body":{
          "app_id":"",
          "sdk_ver":"",
          "pkg":"",
          "ver":"",
          "signature_sha1":"",
          "os":0,
          "osv":"",
          "brand":"",
          "model":"",
          "imei":"",
          "oaid":"",
          "android_id":"",
          "data": {
              "mode":"",	// SCAN/NEW/MATCH
              "list":[
                  {
                      
                  }
              ]
          }
      }
}
  ```
  
  

