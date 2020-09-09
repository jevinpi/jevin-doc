```js
// 列车进出站, exchange: cw.train
// trainStatus: 0-进站 1-出站 direction： 0- 上行 1-下行
// 进展
{
	"num": "1127",
	"equipmentStatus": "0", 
	"standingTime": "120",
	"direction": "0",
	"arrivalTime": "2020-07-22 15:00:00",
	"trainStatus": "0",
	"stationName": "华为",
	"directionName": "双拥街",
	"trainLength": "8"
}
// 出站
{
	"num": "1127",
	"equipmentStatus": "0", 
	"standingTime": "120",
	"direction": "0",
	"arrivalTime": "2020-07-22 15:00:00",
	"trainStatus": "1",
	"stationName": "华为",
	"directionName": "双拥街",
	"trainLength": "8"
}

----------
// 火灾事件，exchange: cw.tempfire
//locationFlag: STATION-站内消防事件TRAIN-隧道区间消防事件
// 站内消防事件
{
    "id":"1","id":"1",
    "num":"F1A-001",
    "alarmFlag":"false",
    "location":"A端设备区-环控电",
    "locationNum":"F1A-001",
    "stationName":"华为站",
    "alarmTime":"2020-07-22 15:00:00",
    "locationFlag":"STATION"
}
// 隧道区间消防事件
{
    "id":"1","id":"1",
    "num":"F1A-001",
    "alarmFlag":"false",
    "location":"华为站外",
    "locationNum":"0",
    "stationName":"华为站",
    "alarmTime":"2020-07-22 15:00:00",
    "locationFlag":"TRAIN"
}

//设备，exchange: cw.charge.equipment
//alarmLevel 0是正常  equipmentStatus：扶梯 垂梯 【up/down/breakdown/close】  alarmLevel： 0 -会恢复报警 >0 则会报警
// 会根据equipmentNum更改 equipmentStatus、alarmLevel、equipmentLocation 的值
// 恢复正常
{
    "systemName":"FAS",
    "stationName":"华为",
    "equipmentType":"扶梯",
    "equipmentName":"扶梯3",
    "equipmentNum":"HW_BAS_16",
    "equipmentLocation":"",
    "equipmentStatus":"down",
    "alarmLevel":"0",
    "data":"下行",
    "alarmTime":"2020-04-26 18:53:00"
}
// 异常

{
    "systemName":"FAS",
    "stationName":"华为",
    "equipmentType":"扶梯",
    "equipmentName":"扶梯7",
    "equipmentNum":"HW_BAS_14",
    "equipmentLocation":"",
    "equipmentStatus":"breakdown",
    "alarmLevel":"1",
    "data":"下行",
    "alarmTime":"2020-04-26 18:53:00"
}

```



