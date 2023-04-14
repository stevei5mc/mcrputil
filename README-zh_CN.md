# mcrputil

![license](https://img.shields.io/badge/License-Apache_2.0-blue.svg)
![version](https://img.shields.io/badge/Version-1.1.5-green.svg)

[![Lang-English](https://img.shields.io/badge/Lang-English-brightgreen)](README.md)

一个用于Minecraft(我的世界)资源包加密和解密的工具

## 使用方法

mcrputil 是一个命令行工具没有gui

```
使用命令: mcrputil <子命令>

子命令:
  encrypt  用于加密资源包的命令(会自动生成密钥)
  decrypt  用于解密资源包的命令(需要指定密钥)
  help     获得命令的帮助

子选项:
  -h, --help  获得命令的帮助
```

### 加密

```
使用命令: mcrputil encrypt [子选项] <输入文件夹> <输出文件夹>

说明:
  <输入文件夹>  源文件(未经加密的!!!)
  <输出文件夹>  加密后的成品

子选项(可选):
  -k, --key <KEY>          指定加密密钥
  -e, --exclude <EXCLUDE>  指定不会被加密的文件
  -h, --help               获得命令的帮助
```

#### 使用方法

1. 请确保你的资源包文件中包含有manifest.json
2. 使用命令 mcrputil encrypt <输入文件夹的路径> <输出文件夹的路径>
3. 一个＜您的输出文件夹的名称＞.key文件和一个contents.json现在应该在您的包/输出文件夹中
4. 在输出文件夹中创建一个压缩包，并且重命名与创建的zip文件（MyPack.zip.key）

示例: 
|文件名|
|-|
|MyPack.zip|
|MyPack.zip.key|

### 解密

```
使用命令: mcrputil decrypt [子选项] <输入文件夹> <输出文件夹>

说明:
  <输入文件夹>  解密前的文件
  <输出文件夹>  解密后的文件

子选项(可选):
  -k, --key <KEY>  指定解密密钥(给没有跟输入文件夹同名的密钥文件使用)
  -h, --help       获得命令的帮助
```
Please make sure, to not publish any of the resulting files, or only with the consent of the copyright holder, as it is
a violation, and note that there will be no support for decrypting resource packs.