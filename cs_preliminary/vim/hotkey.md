# vim 普通模式编辑
-  控制光标移动方向
    `h j k l`
- 翻页
  - `ctrl B` 向前翻页
  - `ctrl F` 向后翻页
  - `ctrl E` 向前翻页一行
  - `ctrl Y` 向后翻页一行
- 跳转
  - `G` 跳转到文本最后
  - `gg` 跳转到文本开头
  - `0` 跳转到本行开头
  - `^` 跳转到本行的首个字符
  - `$` 跳转到本行末尾
  - `w` 去到下一个单词的开头
  - `b` 回到上一个单词的开通要
  - `e` 去到下一个单词的末尾
  - `W` 大跳
  - `B` 大跳
  - `E` 大跳
- 删除
  - `x` 删除光标所在处的单词
  - `dw` 删除光标后面的整个单词
  - `dd` 删除一整行
- 复制粘贴
  - `y` 复制
  - `p` 粘贴
  - `r` 替换一个字符
- 缩进
  - `>>`
  - `<<`
---

# 视图模式
- `v` 进入视图模式
- `o` 反转光标方向

# 撤销
- `u` 退一次
- `CTRL + R` 进一次
---
# 命令模式
- 查找与替换
  - /word + n
  - `:/s/word_before_replace/word_after_replace/g` 全局替换单词
  - `:1,100/s/word_before/word_after` 指定行数替换  