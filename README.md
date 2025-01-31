```text
   ____                _____          ____                    __  _
  / __/__ ____ __ __  / ___/__  ___  / _(_)__ ___ _________ _/ /_(_)__  ___
 / _// _ `(_-</ // / / /__/ _ \/ _ \/ _/ / _ `/ // / __/ _ `/ __/ / _ \/ _ \
/___/\_,_/___/\_, /  \___/\___/_//_/_//_/\_, /\_,_/_/  \_,_/\__/_/\___/_//_/
             /___/                      /___/
```

# EasyConfiguration

[![version](https://img.shields.io/github/v/release/CarmJos/EasyConfiguration)](https://github.com/CarmJos/EasyConfiguration/releases)
[![License](https://img.shields.io/github/license/CarmJos/EasyConfiguration)](https://www.gnu.org/licenses/lgpl-3.0.html)
[![workflow](https://github.com/CarmJos/EasyConfiguration/actions/workflows/maven.yml/badge.svg?branch=master)](https://github.com/CarmJos/EasyConfiguration/actions/workflows/maven.yml)
[![CodeFactor](https://www.codefactor.io/repository/github/carmjos/easyconfiguration/badge)](https://www.codefactor.io/repository/github/carmjos/easyconfiguration)
![CodeSize](https://img.shields.io/github/languages/code-size/CarmJos/EasyConfiguration)
![](https://visitor-badge.glitch.me/badge?page_id=EasyConfiguration.readme)

轻松(做)配置，简单便捷的通用配置文件加载、读取与更新工具，可自定义配置格式。

## 优势

- 基于类的配置文件初始化、加载、获取与更新机制，方便快捷。
- 支持复杂配置的手动序列化、反序列化。
- 提供多种builder形式，快速构建 `ConfigValue<?>` 对象。
- 支持通过注解规定配置对应的路径、注释等信息。

## 开发

详细开发介绍请 [点击这里](.documentation/README.md) , JavaDoc(最新Release) 请 [点击这里](https://CarmJos.github.io/EasyConfiguration) 。

### 示例代码

您可以 [点击这里](demo/src/main/java/cc/carm/lib/configuration/demo/DatabaseConfiguration.java) 查看部分代码演示，更多演示详见 [开发介绍](.documentation/README.md) 。

### 依赖方式

#### Maven 依赖

<details>
<summary>远程库配置</summary>

```xml

<project>
    <repositories>

        <repository>
            <!--采用Maven中心库，安全稳定，但版本更新需要等待同步-->
            <id>maven</id>
            <name>Maven Central</name>
            <url>https://repo1.maven.org/maven2</url>
        </repository>
  
        <repository>
            <!--采用github依赖库，实时更新，但需要配置 (推荐) -->
            <id>EasyConfiguration</id>
            <name>GitHub Packages</name>
            <url>https://maven.pkg.github.com/CarmJos/EasyConfiguration</url>
        </repository>

        <repository>
            <!--采用我的私人依赖库，简单方便，但可能因为变故而无法使用-->
            <id>carm-repo</id>
            <name>Carm's Repo</name>
            <url>https://repo.carm.cc/repository/maven-public/</url>
        </repository>

    </repositories>
</project>
```

</details>

<details>
<summary>通用原生依赖</summary>

```xml

<project>
    <dependencies>
        <!--基础实现部分，需要自行实现“Provider”与“Wrapper”。-->
        <dependency>
            <groupId>cc.carm.lib</groupId>
            <artifactId>easyconfiguration-core</artifactId>
            <version>[LATEST RELEASE]</version>
            <scope>compile</scope>
        </dependency>

        <!--基于YAML文件的实现版本，可用于全部Java环境。-->
        <dependency>
            <groupId>cc.carm.lib</groupId>
            <artifactId>easyconfiguration-yaml</artifactId>
            <version>[LATEST RELEASE]</version>
            <scope>compile</scope>
        </dependency>

        <!--基于JSON文件的实现版本，可用于全部Java环境。-->
        <!--需要注意的是，JSON不支持文件注释。-->
        <dependency>
            <groupId>cc.carm.lib</groupId>
            <artifactId>easyconfiguration-json</artifactId>
            <version>[LATEST RELEASE]</version>
            <scope>compile</scope>
        </dependency>

    </dependencies>
</project>
```

</details>

#### Gradle 依赖

<details>
<summary>远程库配置</summary>

```groovy
repositories {

    // 采用Maven中心库，安全稳定，但版本更新需要等待同步 
    mavenCentral()
  
    // 采用github依赖库，实时更新，但需要配置 (推荐)
    maven { url 'https://maven.pkg.github.com/CarmJos/EasyConfiguration' }

    // 采用我的私人依赖库，简单方便，但可能因为变故而无法使用
    maven { url 'https://repo.carm.cc/repository/maven-public/' }
}
```

</details>

<details>
<summary>通用原生依赖</summary>

```groovy

dependencies {

    //基础实现部分，需要自行实现“Provider”与“Wrapper”。
    api "cc.carm.lib:easyconfiguration-core:[LATEST RELEASE]"

    //基于YAML文件的实现版本，可用于全部Java环境。
    api "cc.carm.lib:easyconfiguration-yaml:[LATEST RELEASE]"

     //基于JSON文件的实现版本，可用于全部Java环境。
    //需要注意的是，JSON不支持文件注释。
    api "cc.carm.lib:easyconfiguration-json:[LATEST RELEASE]"

}
```

</details>

## 衍生项目

### [**MineConfiguration**](https://github.com/CarmJos/MineConfiguration) (by @CarmJos )

EasyConfiguration for MineCraft!
开始在 MineCraft 相关服务器平台上轻松(做)配置吧！

目前支持 BungeeCord, Bukkit(Spigot) 服务端，后续将支持更多平台。

## 支持与捐赠

若您觉得本插件做的不错，您可以通过捐赠支持我！

感谢您对开源项目的支持！

<img height=25% width=25% src="https://raw.githubusercontent.com/CarmJos/CarmJos/main/img/donate-code.jpg"  alt=""/>

## 开源协议

本项目源码采用 [GNU LESSER GENERAL PUBLIC LICENSE](https://www.gnu.org/licenses/lgpl-3.0.html) 开源协议。
