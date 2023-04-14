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

#### Step-by-step

1. Make sure your pack is unzipped, and in your pack folder should be a manifest.json
2. mcrputil encrypt <path to your unzipped pack folder> <path to your unzipped pack/output folder>
3. A <name of your pack folder>.key file and a contents.json should now be in your pack/output folder
4. Create a zip file with the contents of your pack/output folder, and rename your .key file to the same name as the
   created zip file (MyPack.zip.key)

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