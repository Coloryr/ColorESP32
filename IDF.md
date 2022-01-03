# ESP-IDF安装
一个简明的安装教程

[返回](/README.md)

## 下载工具

[git软件](https://git-scm.com/downloads)  
[python软件](https://www.python.org/downloads/)  

### 下载完后安装

[pip安装脚本](https://bootstrap.pypa.io/get-pip.py)

```
python get-pip.py
```

### 添加环境变量

`Python路径`  
`Python路径\Scripts`


### IDE选择

[Vscode](https://code.visualstudio.com/)  
[Clion](https://www.jetbrains.com/clion/)

## 开始步骤

在你想要安装esp-idf的目录新建文件夹
```
git clone https://github.com/espressif/esp-idf.git
```

添加环境变量

- `IDF_PATH`：`ESP-IDF克隆的目录`
- `IDF_TOOLS_PATH`：`你想让esp-idf工具安装的目录`

例如：

- `IDF_PATH`：`G:\espidf\esp-idf`
- `IDF_TOOLS_PATH`：`G:\espidf\env`

在`ESP-IDF克隆的目录`打开命令行  
执行命令
```
.\install.bat
```
或
```
.\install.bat ESP32S3
```
之后再
```
pip install -r .\requirements.txt
```

等待安装完成，出现错误自行解决  
安装完成后
```
.\export.bat
```

上面会出现一堆PATH
除了`python_env\idf5.0_py3.10_env\Scripts`，其他全部添加进环境变量的`path`

完成后输入
```
cmake
xtensa-esp32s3-elf-gcc -v
idf.py
```

若均无报错则安装完成