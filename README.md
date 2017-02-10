#高德地图定位Android版插件
本插件利用高德地图提供的定位功能进行Android版手机定位。
  
####为什么没有iOS版？
因为iOS版有官方的定位插件_cordova-plugin-geolocation_可以使用。

请参照：[cordova-plugin-geolocation](https://github.com/apache/cordova-plugin-geolocation)

####Android版为什么不使用官方的_cordova-plugin-geolocation_插件
最新版的插件已经删除掉的Android版定位的代码，改为基于系统浏览器(chrome内核)进行定位。

为什么这样做，也有人问过同样的问题，作者的回答是这样比原生定位更快更准确。

但经过测试后，发现根本无法定位，几经调查发现跟貌似国内网络有关系，原因相信大家都懂的，此过省略好几个字。。。。

__此插件就这么诞生了__

####版本
基于高德地图Android版定位SDK

####一，申请密钥
请参照：[申请密钥Android定位SDK](http://lbs.amap.com/api/android-location-sdk/guide/create-project/get-key/)

####二，安装插件

```
cordova plugin add https://github.com/mrwutong/cordova-qdc-baidu-location --variable API_KEY=your key

```

####三，使用方法

```
// 进行定位
GaoDe.getCurrentPosition(successCallback, failedCallback);
```

获得定位信息，返回JSON格式数据:

```
{
  latitude : 纬度,
  lontitude: 经度,
  ...
}
```
####四，查看当前安装了哪些插件

```
ionic plugin ls
```

####五，删除插件

```
ionic plugin rm com.qdc.plugins.baidu.location
```








