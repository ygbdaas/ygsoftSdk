# YGSOFT IoT Device SDK for JAVA

## 通过Maven来安装SDK

下载完[ygsoftest-0.0.1-SNAPSHOT-jar-with-dependencies](https://github.com/ygbdaas/YGMQTTSample/raw/master/ygsoftest-0.0.1-SNAPSHOT-jar-with-dependencies.jar)的jar包之后 ，将jar包添加到本地的maven仓库中
使用以下命令:
```
mvn install:install-file -Dfile=dfile -DgroupId=groupid -DartifactId=artifactid -Dversion=version -Dpackaging=jar
```

添加完之后，在项目中导入依赖：
```
<dependency>
      <groupId>com.ygsoft.iot</groupId>
      <artifactId>ygsoftiotsdk</artifactId>
      <version>1.0.0</version>
</dependency>
```

## 发布服务：

初始化YGSOFTClient
YGSOFTClient ygsoftClient = YGSOFTClient.initClient(certificatefile,privateKeyFile);


ygsoftiotpublishSample：初始化ygsoftiot核心类
certificatefile：证书的本地路径
privateKeyFile ：私钥的本地路径
```

### 创建自己的消息类继承提供的基类basement:
```
NewBasement extends Basement{}
```

说明：
```
在基础的属性上增加其余的属性
```

### 发布消息:
ygsoftClient.publish(Basement)


ygsoftClient.publish(List<T extends Basement>)


