## nCov2019-show

基于`api`接口和`Redis`实现的疫情展示

## 接口及实现

使用的数据是天行数据提供的免费接口以及网易的实时数据接口

天行数据的两个接口：

https://www.tianapi.com/gethttp/169

https://www.tianapi.com/gethttp/170

网易提供的实时数据接口：

https://c.m.163.com/ug/api/wuhan/app/index/feiyan-data-list

为了不多次的访问网络接口，从这三个接口中获取到数据后，都保存到了本地的 `redis` 中，这样只需要每隔一段时间访问上面的三个接口即可，其余 `web` 页面的请求都从 `redis` 中获取。

## 使用

本地环境安装[Redis](https://github.com/MicrosoftArchive/redis/releases)

> 安装的时候一定要`ADD PATH`

数据抓取：
```python
python GetData.py
```

数据展示：
```python
python run.py
```

打开`127.0.0.1:5000` 查看效果~

## 参考

https://www.imooc.com/article/300555




