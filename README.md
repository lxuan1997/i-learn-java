# java

## java 环境准备

1. [下载 JDK](https://www.oracle.com/cn/java/technologies/downloads/)（以**JDK17**为例）

2. 安装

3. 设置`java`环境变量

| 变量      | 值               |
| --------- | ---------------- |
| JAVA_HOME | D:\Java\jdk-17\  |

4. 添加`Path`环境变量

```
%JAVA_HOME%\bin
```

5. 检查`java`是否安装成功

- 任意目录位置打开 `cmd` 窗口，输入以下命令

```sh
java --version
```

- 控制台输出

```sh
java 17.0.8 2023-07-18 LTS
Java(TM) SE Runtime Environment (build 17.0.8+9-LTS-211)
Java HotSpot(TM) 64-Bit Server VM (build 17.0.8+9-LTS-211, mixed mode, sharing)
```

## 可执行文件
- **java**：这个可执行程序其实就是`JVM`，运行`Java`程序，就是启动`JVM`，然后让`JVM`执行指定的编译后的代码；
- **javac**：这是Java的编译器，它用于把`Java`源码文件（以`.java`后缀结尾）编译为`Java`字节码文件（以`.class`后缀结尾）；
- **jar**：用于把一组`.class`文件打包成一个`.jar`文件，便于发布；
- **javadoc**：用于从`Java`源码中自动提取注释并生成文档；
- **jdb**：`Java`调试器，用于开发阶段的运行调试。