# mavenUpload
-------------
上传aar至maven repo
-------------

以上传名为`library`的module为例：

 1.将mavenUpload.gradle到工程根目录
 2.将gradle.properties放到`library`中，并配置信息
```
MAVEN_REPO_RELEASE=http://localhost:8081/repository/Release/
MAVEN_REPO_SNAPSHOT=http://localhost:8081/repository/Snapshot/

MAVEN_REPO_USERNAME=admin
MAVEN_REPO_PASSWORD=admin123

MAVEN_REPO_GROUP=io.auxo.library
MAVEN_REPO_ARTIFACT=library
MAVEN_REPO_VERSION=1.0
```
 3.在`library`的build.gradle中加入
```
apply from: "../mavenUpload.gradle"
```
 4.执行`gradlew clean :library:uploadArchives`
