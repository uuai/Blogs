#字符串转换为驼峰结构#

```
// 字符串转换为驼峰结构
function doStr(str){

	// 转换为数组
	var strArr = str.split("");

	// 循环数组
	for(var i=0; i<strArr.length; i++){

		// 移除 - 字符
		if(strArr[i] == "-"){

			// 删除匹配到的 - 符号
			strArr.splice(i,1);

			// 如果不是第一个，替换之后字母为大写
			if(i!==0){

				// 如果 - 后面不为空
				if(strArr[i]!==""){
					strArr[i] = strArr[i].toUpperCase();
				}
			}
		}

	}
	// 数组转换为字符串
	var str = strArr.join("");
	return str;

}
document.write("-webkit-border-image ==>>> "+doStr("-webkit-border-image"));
```

##示例：

```
-webkit--border-image  ==>>>  webkitBorderImage
```