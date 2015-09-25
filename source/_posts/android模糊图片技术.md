title: android模糊图片技术
date: 2015-09-25 14:54:52
tags: android 图片
categories: android

---
RenderScript是android的计算图形框架。android的动态墙纸就是用了这一技术。本文学习一下把一张图片进行模糊显示处理。
<!--more-->

# 集成Renderscript Support支持库  #
## 使用Gradle配置 ##
在项目的build.gradle添加以下代码
```
android {
    defaultConfig {
        renderscriptTargetApi 19
        renderscriptSupportModeEnabled true
    }
}
```
添加成功后，会发现`android.support.v8.renderscript.*`的类可以使用

## 使用RenderScript模糊图片 ##
以下是模糊的核心代码
```
public class BlurBuilder {
    private static final float BITMAP_SCALE = 0.4f;
    private static final float BLUR_RADIUS = 7.5f;

    public static Bitmap blur(Context context, Bitmap image) {
        int width = Math.round(image.getWidth() * BITMAP_SCALE);
        int height = Math.round(image.getHeight() * BITMAP_SCALE);

        Bitmap inputBitmap = Bitmap.createScaledBitmap(image, width, height, false);
        Bitmap outputBitmap = Bitmap.createBitmap(inputBitmap);

        RenderScript rs = RenderScript.create(context);
        ScriptIntrinsicBlur theIntrinsic = ScriptIntrinsicBlur.create(rs, Element.U8_4(rs));
        Allocation tmpIn = Allocation.createFromBitmap(rs, inputBitmap);
        Allocation tmpOut = Allocation.createFromBitmap(rs, outputBitmap);
        theIntrinsic.setRadius(BLUR_RADIUS);
        theIntrinsic.setInput(tmpIn);
        theIntrinsic.forEach(tmpOut);
        tmpOut.copyTo(outputBitmap);

        return outputBitmap;
    }
}
```
只需要适当地调整`BITMAP_SCALE`和`BLUR_RADIUS`这两个参数就可以了。
注意一点的是。导入的包一定要是`android.support.v8.renderscript.*`，不然就只能在Api 17(Android 4.3)的版本上使用。

如果要对一张Bitmap图片进行模糊，只需要调用上面的blur方法，生成一个新的Bitmap就可以了。
```
Bitmap blurredBitmap = BlurBuilder.blur( getActivity(), originalBitmap );
view.setBackgroundDrawable( new BitmapDrawable( getResources(), blurredBitmap ) );
```
这是原图
![](http://i.imgur.com/Fm1AbGY.jpg)

压缩后的图片
![](http://i.imgur.com/8wnvB99.jpg)