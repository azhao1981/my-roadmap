# sed

## TIPS

+ sed是一个很重要的文本替换工具,在批量修改文件相当有用
+ 如果使用mac,强烈推荐安装 gsed

## 命令

### 匹配行前后添加
```bash
#匹配行前加
sed -i '/allow 361way.com/iallow www.361way.com' the.conf.file
#匹配行前后
sed -i '/allow 361way.com/aallow www.361way.com' the.conf.file
```

### 删除最后几行

 A=$(sed -n '$=' a.txt)
 sed $(($A-3+1)),${A}d a.txt
或者使用上面两条命令。删除的是倒数3行的。
如果删除倒数300 ，那就把3改为300 就可以了。
 cat aa.txt
aaaa
bbbb
cccc
dddd
eeee
 sed '2,$d' -i aa.txt
-i 是要在原文件上修改。如果不需要修改，就不用i 了。
 cat aa.txt
aaaa

其中 ，sed '2,$d' -i aa.txt
这条命令是 删除从第2行（包括第2行）到文件末尾的所有行。

### 上下几行

https://zhidao.baidu.com/question/872073677553672012.html
sed '/Mac address/,+3d;:go;1!{P;$!N;D};N;bgo' file

### 代替

```
grep -rl '52698' /usr/local/bin/ratom  | xargs sed -i 's/52698/53698/g'
```

## mac sed

xshell

-i 修改
-e 只读

grep -l 10.1.251.4 *.yml | head -n 1 | xargs sed -i '' '/10.1.251.4/i\
ipip_redis:\
\ \ host: 10.1.251.174\
\ \ port: 6379\
'

sed -i '' '/10.1.251.4/i\
ipip_redis:\
\ \ host: 10.1.251.174\
\ \ port: 6379\
'  test.b1_39.107.12.131_property.yml

http://zhouxiaohong.com/2016/08/02/sed-in-mac/


sed -i '' '1i\ hello ' hello.php
上面这行代码，作用是往文件中插入 hello ，在 linux 下可以正常运行，但是在 Mac 上，啊哦，报错。原因是使用 sed 命令往文件中插入文本时，必须在 1i 后面插入一个换行符正确代码如下。例如你要在终端使用此命令，正确代码如下，在 1i 后，敲个回车，然后继续输入后面的命令。

sed -i '' '1i\
hello' hello.php
因为我是使用 ruby 来调用 shell 脚本，因此会将命令写在字符串中，在 ruby 中使用 sed 插入文本的代码如下。

system "sed -i '' '1i\\'$'\n''hello' hello.php"
这些都是血的教训啊。。。。。。。

用gsed

http://itaofe.info/sed-%E5%9C%A8mac%E4%B8%8B%E6%97%A5%E5%B8%B8%E4%BD%BF%E7%94%A8%E7%9A%84%E5%B7%AE%E5%BC%82/


### 错误提示

```bash
# 错误: 后面不要加这个 '\'
gsed -i '$a\ali_oss_internal_host_url: oss-cn-hangzhou-internal.aliyuncs.com
ali_oss_public_host_url:   oss-cn-hangzhou.aliyuncs.com
\' config/property/*.yml

# 正确
gsed -i '$a\ali_oss_internal_host_url: oss-cn-hangzhou-internal.aliyuncs.com\
ali_oss_public_host_url:   oss-cn-hangzhou.aliyuncs.com\
' config/property/try.property.yml
```

