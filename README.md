[![](https://jitpack.io/v/pao11/GuideViewRelease.svg)](https://jitpack.io/#pao11/GuideViewRelease)
[![Travis](https://img.shields.io/badge/Gradle-2.3.1-brightgreen.svg)]()

# 概况
功能导航页view
====
应用推出新功能需要给给用户提示指引一下.传入需要指引的View即可

<table>
    <tr>
        <td><img src="/screenshots/guide1.jpg"></td>
        <td><img src="/screenshots/guide2.jpg"></td>
        <td><img src="/screenshots/guide3.jpg"></td>
    </tr>
</table>

How To Useage
----
使用方法
-

step1.Add it in your root build.gradle at the end of repositories:
-
第一步：在项目根目录的gradle文件中添加以下代码
-
    allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

Step 2. Add the dependency
-
第二步：增加依赖
-
    dependencies {
	        compile 'com.github.pao11:GuideViewRelease:v1.0.0'
	}

使用示例
=
布局文件中引入UserGuideView：
````
<com.pao11.guideview.UserGuideView
        android:id="@+id/guideView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:HighlightViewStyle="circle"
        app:MaskBlurStyle="solid"
        app:maskColor="#aa565656"
        app:tipView="@mipmap/tip_view" />

````
然后：
````
    guideView.setHighLightView(targetView);
````
````
例如：
  ImageView icon = (ImageView) findViewById(R.id.icon);
  guideView.setHighLightView(icon);
````
属性说明
=
支持高亮框形状 属性app:HighlightViewStyle="oval" 方形 圆形 椭圆 可选(oval,rect,circle)

提示的图片  属性 app:tipView="@mipmap/tip_view"

蒙版层颜色 属性 app：maskColor

高亮框边缘模糊效果 属性  app:MaskBlurStyle="solid" normal/solid

更新记录
=


**v1.0.0**　`2017.09.07`　发布第一版本

## Copyright Notice ##
``` 
Copyright (C) 2017 pao11

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
 ```




