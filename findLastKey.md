# lodash源码分析之findLastKey

本文为读 lodash 源码的第二百八十八篇，后续文章会更新到这个仓库中，欢迎 star：[pocket-lodash](https://github.com/yeyuqiudeng/pocket-lodash)

gitbook也会同步仓库的更新，gitbook地址：[pocket-lodash](https://www.gitbook.com/book/yeyuqiudeng/pocket-lodash/details)

## 依赖

```javascript
import baseFindKey from './.internal/baseFindKey.js'
import baseForOwnRight from './.internal/baseForOwnRight.js'
```

[《lodash源码分析之baseFindKey》](internal/baseFindKey.md)

[《lodash源码分析之baseForOwnRight》](internal/baseForOwnRight.md)

## 源码分析

`findLastKey` 和 `findKey` 的作用差不多，不过遍历的顺序是从后往前。

源码如下：

```javascript
function findLastKey(object, predicate) {
  return baseFindKey(object, predicate, baseForOwnRight)
}
```

传入 `baseFindKey` 的迭代函数 `eachFunc` 为 `baseForOwnRight` ，即从后向前遍历。

## License 

[署名-非商业性使用-禁止演绎 4.0 国际 (CC BY-NC-ND 4.0)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

最后，所有文章都会同步发送到微信公众号上，欢迎关注,欢迎提意见：  ![](https://raw.githubusercontent.com/yeyuqiudeng/resource/master/images/qrcode_front-end-article.jpg) 

作者：对角另一面 