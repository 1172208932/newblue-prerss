## 4.1打开客户端原生页面

```js
api_name: 'cztvRouter'
data: {
 route: '', // schemeurl
}
success: function(res) {   // 调用成功的回调}
```
route后缀中的path、url等参数，均需经过encodeURIComponent编码， 透传参数自行拼接

## 4.1.1 点播落地页
```js
route: chinablue://cztvrouter/feed/vod?pageId=100164
// pageId: 点播页视频id 
```
4.1.2 短视频落地页
```js

route: chinablue://cztvrouter/feed/shorts?pageId=221
// pageId: 短视频id
```
4.1.3 活动直播页
```js

route: chinablue://cztvrouter/feed/live_activity?pageId=680
// pageId: 直播id
```
4.1.5 UGC图文落地页
```js
route: chinablue://cztvrouter/ugc/photo_article?uid=25494634
// uid: 关联id, sns的uid
```
4.1.6 UGC音频落地页
```js
route: chinablue://cztvrouter/ugc/music_detail?uid=25494634
// uid: 关联id, sns的uid
```
4.1.7个人号主页
```js
route: chinablue://cztvrouter/ugc/user_center?uid=100
// uid: 关联id, sns的uid
```
4.1.8 ugc动态发布页
```js
route: chinablue://cztvrouter/ugc/post_dynamic
```
4.1.9 ugc视频发布页
```js
route: chinablue://cztvrouter/ugc/post_video
```
4.1.14 部落首页
```js
route: chinablue://cztvrouter/business/tribe
```
4.1.15 音频ktv
```js
route: chinablue://cztvrouter/business/ktv?sessionId=111
// sessionId: 用户sessionId
```
4.1.16 微信小程序
```js
route: chinablue://cztvrouter/wx/miniapp?userName=gh_d43f693ca31f&path=page%2Fanimation%2Findex&miniProgramType=0
// useName: 微信小程序原始id
// path: 可选，小程序指定页面路径，需要编码
// miniProgramType: 可选，小程序类型（0=正式版，1=开发版，2=体验版）

res返回值：
成功 {“code“:200,”msg”:”调用成功”}
失败 {“code“:500,”msg”:”调用失败”}
```