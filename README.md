# 如何将自己的Android代码上传到github上，以后项目直接引用。
AndroidStudio使用gradle来编译项目，当我们需要使用第三方lib库时，只需要简简单单一行代码就可以引入第三方库，给我开发带来很大的方便。那怎么把自己的一些经验代码也像第三方库那样一句代码引入到其它项目中呢？
## 1、创建lib库项目
1）使用AndroidStudio工具，像创建普通Android项目一样创建一个项目。把需要的工具类和资源文件写入或拷贝到刚创建项目中，保证项目能正常编译运行。
2）将app的gradle文件开头的 apply plugin: 'com.android.application' 改成 apply plugin: 'com.android.library'，把他变成一个lib项目
3）将app的gradle文件中的 applicationId "你的报名" 这个代码去掉，因为它是一个lib库，applicationId跟随引用它的主项目，lib库不需要applicationId
4）去掉AndroidManifest.xml文件中的主Activity配置

### 这个是三个井号标题
123
### 这里是标题
