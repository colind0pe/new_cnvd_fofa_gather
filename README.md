# new_cnvd_fofa_gather

## 0x00 前言

本项目是对对项目：https://github.com/RaiderZP/cnvd_fofa_gather 进行的修改，更改为使用FOFA官方提供的查询接口。本项目去除了原项目中的代理池功能，通过设置5秒的访问间隔时间来保证查询的成功率。

## 0x01 简介

通过公司名称，在fofa上搜索可能存在通用产品的公司，原理是判断网站标题数目以及独立IP数达到一定条件时将该标题以及公司名称导出；如果想挖掘cnvd证书，可导出注册资金大于5000w的公司到这个脚本中进行通用系统收集。

## 0x02 使用方法

修改脚本第10、11行为你的FOFA账号的邮箱和API KEY

```python
# 填入fofa账号的email和API_KEY
email = 'YOUR_EMAIL'
api_key = 'API_KEY'
```

将公司名称放入`gs.txt`文件中，执行该脚本即可。

```python
python3 new_cnvd_fofa_gather.py
```



