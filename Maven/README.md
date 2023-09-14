# Maven

`Maven`是一个`Java`项目管理和构建工具，它可以定义项目结构、项目依赖，并使用统一的方式进行自动化构建，是`Java`项目不可缺少的工具。

## Maven 主要功能

- 提供了一套标准化的项目结构；
- 提供了一套标准化的构建流程（编译，测试，打包，发布……）；
- 提供了一套依赖管理机制。

## Maven 项目结构

一个使用 Maven 管理的普通的 Java 项目，它的目录结构默认如下：

```
a-maven-project（根目录）
├── pom.xml（项目描述文件）
├── src
│   ├── main
│   │   ├── java（Java源码）
│   │   └── resources（资源文件）
│   └── test
│       ├── java（测试源码）
│       └── resources（测试资源文件）
└── target（编译、打包生成的文件）
```

### 项目描述文件 pom.xml

示例：

```xml
<project ...>
	<modelVersion>4.0.0</modelVersion>
	<groupId>com.itranswarp.learnjava</groupId>
	<artifactId>hello</artifactId>
	<version>1.0</version>
	<packaging>jar</packaging>
	<properties>
        ...
	</properties>
	<dependencies>
        <dependency>
            <groupId>commons-logging</groupId>
            <artifactId>commons-logging</artifactId>
            <version>1.2</version>
        </dependency>
	</dependencies>
</project>
```

- `groupId` 类似于 `Java` 的包名，通常是公司或组织名称
- `artifactId` 类似于 `Java` 的类名，通常是项目名称
- `version`，项目版本号

一个`Maven`工程就是由`groupId`，`artifactId`和`version`作为唯一标识。

我们在引用其他第三方库的时候，也是通过这 3 个变量确定，例如，依赖`commons-logging`，使用`<dependency>`声明一个依赖后，`Maven`就会自动下载这个依赖包并把它放到`classpath`中。

```xml
<dependency>
    <groupId>commons-logging</groupId>
    <artifactId>commons-logging</artifactId>
    <version>1.2</version>
</dependency>
```

## Maven 安装

1. [下载](https://maven.apache.org/download.cgi)

2. 本地解压（D:\apache-maven-3.8.6）

3. 设置`Maven`环境变量

| 变量       | 值                    |
| ---------- | --------------------- |
| MAVEN_HOME | D:\apache-maven-3.8.6 |

4. 添加`Path`环境变量

```
%MAVEN_HOME%\bin
```

5. 检查`Maven`是否安装成功

- 任意目录位置打开 `cmd` 窗口，输入以下命令

```sh
mvn --version
```

- 控制台输出

```sh
Apache Maven 3.8.6 (84538c9988a25aec085021c365c560670ad80f63)
Maven home: D:\apache-maven-3.8.6
Java version: 17.0.8, vendor: Oracle Corporation, runtime: D:\Java\jdk-17
Default locale: zh_CN, platform encoding: GBK
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```

