# 歌曲词云

## 获取歌词接口：
https://c.y.qq.com/soso/fcgi-bin/client_search_cp?t=7&p=1&n=10&w=%E6%B2%B3%E5%9B%BE&format=json

#### 接口分析：
- p: 当前页面
- n: 每面显示的数量
- w: 歌手姓名
- format: 返回格式
#### 注意
经试验，该接口仅能返回至多20页数据，其中大约有110条来自搜索的歌手

## 依赖
基于python3 和 第三方包 `wordcloud`
```
# 安装 wordcloud
$ pip install wordcloud

# 安装 jieba 分词
$ pip install jieba
```
## 用法
```
# 下载歌词
$ python download.py 周杰伦

# 分析歌词并绘制词云
$ python analyse.py 周杰伦
```

## 关于词云的形状
如果在对应歌手的目录有图片 `bg.jpg` ,则以此图片为依据绘制词云，如果在歌手目录未来发现，则用根目录下的 `bg.jpg` 为依据绘制词云。
