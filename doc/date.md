# 时间格式化

> RegExp、Date

```javascript
// date 为Date对象
// fmt 格式化 YYYY-MM-dd  HH:mm:ss 
function formatDate (date, fmt) {
  if (/(Y+)/.test(fmt)) {
    fmt = fmt.replace(RegExp.$1, (date.getFullYear()+'').substr(4-RegExp.$1.length))
  }
  let o = {
    'M+': date.getMonth() + 1,
    'd+': date.getDate(),
    'h+': date.getHours(),
    'm+': date.getMinutes(),
    's+': date.getSeconds()
  };
  for (let k in o) {
    if (new RegExp(`${k}`).test(fmt)) {
      let str = o[k] + '';
      fmt = fmt.replace(RegExp.$1, (RegExp.$1.length===1)?str:padLeftZero(str));
      // RegExp.$1.length===1 不加0的情况
    }
  }
  return fmt;
};

function padLeftZero (str) {
  return (('00'+str).substr(str.length));
}

```
RegExp.$1为构造属性，在调用 exec() 或 test() 方法时，这些属性($1~$9)会被自动填充。