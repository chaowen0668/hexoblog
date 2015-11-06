title: android wear学习记录
date: 2015-11-06 11:12:05
tags: wear
categories: android

---
学习android wear的开发记录

<!--more-->


# 卡片UI #
有两种方式创建卡片布局.
## 使用CardFragment ##
布局内容:
```
<?xml version="1.0" encoding="utf-8"?>
<android.support.wearable.view.BoxInsetLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent"
    android:layout_height="match_parent" android:id="@+id/container" tools:context=".MainActivity"
    tools:deviceIds="wear">
    <FrameLayout
        android:id="@+id/frame_layout"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:layout_box="bottom">

    </FrameLayout>

</android.support.wearable.view.BoxInsetLayout>
```

MainActivity.java
```
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        FragmentManager fragmentManager = getFragmentManager();
        FragmentTransaction fragmentTransaction = fragmentManager.beginTransaction();
        CardFragment cardFragment = CardFragment.create("标题 ",
               "内容",
                R.mipmap.ic_launcher);
        cardFragment.setCardGravity(Gravity.TOP);
        fragmentTransaction.add(R.id.frame_layout, cardFragment);
        fragmentTransaction.commit();
    }
```

## 在布局使用CardFrame ##




