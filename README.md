# mavenUpload
-------------
上传aar至maven repo
-------------

以上传名为`library`的module为例：

 1.在local.properties中添加下列配置信息:  
```
# maven repository url
repo.url.release = http://localhost:8081/repository/maven-releases/
repo.url.snapshot = http://localhost:8081/repository/maven-snapshots/

# username and password
repo.user.name = admin
repo.user.password = admin123

# group:artifact:version
repo.group = io.auxo.library
repo.artifact = library
repo.version = 1.0
```
 2.在`library`的build.gradle中加入  
```
apply from: 'https://raw.githubusercontent.com/4332weizi/mavenUpload/master/mavenUpload.gradle'
```
 3.执行`gradlew clean :library:uploadArchives`  
