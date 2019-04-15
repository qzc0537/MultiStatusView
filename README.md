# MultiStatusView
可切换多种状态的view

[![](https://jitpack.io/v/qzc0537/MultiStatusView.svg)](https://jitpack.io/#qzc0537/MultiStatusView)


使用
--
1.project build.gradle下添加：
maven { url 'https://jitpack.io' }

如下：

```
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```

2.app build.gradle下添加依赖 ：

```
implementation 'com.github.qzc0537:MultiStatusView:1.0.1'
```

3.愉快的使用：
```
    <com.qzc.multistatusview.MultipleStatusView
        android:id="@+id/multipleStatusView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:emptyView="@layout/empty_view"
        app:errorView="@layout/error_view"
        app:loadingView="@layout/loading_view"
        app:noNetworkView="@layout/no_network_view">

        <android.support.v7.widget.RecyclerView
            android:id="@+id/mRecyclerView"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:clipToPadding="false"
            android:paddingBottom="51dp" />
    </com.qzc.multistatusview.MultipleStatusView>
    
    代码中调用：
        mStatusView.showLoading();
        mStatusView.showEmpty();
        mStatusView.showContent();
        ......
