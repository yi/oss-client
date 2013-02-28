<h3>1</h3>
路由：/ios/member/profile/:member_id  <br/>
类型：get  <br/>
功能：根据会员ID获取会员信息  <br/>
返回：<br/>
失败
```json
{"code":"InvalidArgument","message":"member not found"}
```
成功
```json
{
  memberId     : Number,
  userId       : Number,
  merchantId   : Number,
  roleId       : Number,
  petName      : String,
  state        : String,// ['disable', 'enable', 'suspend']
  privacy      : String,// ['notShare', 'baseShare', 'fullShare']
  createdAt    : Date,
  dueTime      : Date,
  point        : Number,
  savings      : Number,
  savingDueTime: Date,
  pushState    : String,// ['receive', 'reject']}
}
```
<h3>2</h3>
路由：/ios/member/bills/:member_id  <br/>
类型：get  <br/>
功能：根据会员ID获取会员消费记录  <br/>
返回：
失败
```json
{
  "code":"InvalidArgument",
  "message":"bills not found"
}
```
成功（返回json数组）
```json
[{
  memberId : Number,
  merchant : String,
  billCode : String,
  posCode  : String,
  points   : Number,
  balance  : String,
  time     : Date
}]
```
<h3>3</h3>
路由：/ios/gifts/:merchant_id  <br/>
类型：get  <br/>
功能：根据商户ID获取商户礼品列表  <br/>
返回：
失败
```
```
成功
```
```
<h3>4</h3>
路由：/ios/activities/:merchant_id
<h3>5</h3>
路由：/ios/gift/infor/:gift_id
post
<h3>1</h3>
路由：/ios/exchange/gifts