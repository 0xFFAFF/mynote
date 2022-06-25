# python中字符串的处理

字符串的内部函数
|function|describle|
|---|---|
|string.capitalize|把字符串的第一个字母大写|
|string.center(width)|字符串居中，字符串长度为width|
|string.count(str,beg=0,end=len(string))|计算某段字符出现的次数，可以设置起始位置和终止位置|
|string.decode()|设置解码格式|
|string.encode()|设置编码格式|
|string.endwith(str,beg,end)|检查字符串是否以str结尾，可以设置起始位置|
|string.expandtabs(tabsize)|将tab转化为空格|
|string.find(str,beg,str)|找到返回索引，找不到返回-1|
|string.format()|格式化字符串|
|string.index(str,beg,end)|功能和find一样，只不过找不到会报错|
|string.isalnum()|检查所有字符是否是数字或者字符|
|string.isalpha()|是否全部为字母|
|string.isdecimal()|是否只包含十进制数字|
|string.isdigital()|是否只包含数字|
|string.islower()|是否全部是小写|
|string.isnumeruc()|string中是否只包含数字字符|
|string.isspace()|是否包含空格|
|string.isupper()|是否全是大写|
|string.istitle()|是否是标题化的|
|string.join(seq)||
|string.lower()|转化为小写|
|string.lstrip()|截掉左边的空格|
|string.maketrans(intab,outab)|maketrans() 方法用于创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标|
|max(str)|返回str中最大的字母|
|min(str)|返回str中最小的字母|
|string.partition(str)|把字符串根据str分为三元素的元组|
|string.replace(str1, str2,  num=string.count(str1))|将str1替换成str2，替换次数为count次|
|string.rfind(str, beg=0,end=len(string) )|类似于 find() 函数，返回字符串最后一次出现的位置，如果没有匹配项则返回 -1|
|string.rindex( str, beg=0,end=len(string))|类似于 index()，不过是返回最后一个匹配到的子字符串的索引号|
|string.rjust(width)|返回一个原字符串右对齐,并使用空格填充至长度 width 的新字符串|
|string.rpartition(str)|类似于 partition()函数,不过是从右边开始查找|
|string.rstrip()|删除 string 字符串末尾的空格|
|string.split(str="", num=string.count(str))|以 str 为分隔符切片 string，如果 num 有指定值，则仅分隔 num+1 个子字符串|
|string.splitlines([keepends])|按照行('\r', '\r\n', '\n')分隔，返回一个包含各行作为元素的列表，如果参数 keepends 为 False，不包含换行符，如果为 True，则保留换行符。|
|string.startswith(obj, beg=0,end=len(string))|检查字符串是否是以 obj 开头，是则返回 True，否则返回 False。如果beg 和 end 指定值，则在指定范围内检查.|
|string.strip([obj])|在 string 上执行 lstrip()和 rstrip()|
|string.swapcase()|翻转 string 中的大小写|
|string.title()|返回"标题化"的 string,就是说所有单词都是以大写开始，其余字母均为小写(见 istitle())|
|string.translate(str, del="")|根据 str 给出的表(包含 256 个字符)转换 string 的字符,要过滤掉的字符放到 del 参数中|
|string.upper()|转换 string 中的小写字母为大写|
|string.zfill(width)|返回长度为 width 的字符串，原字符串 string 右对齐，前面填充0|