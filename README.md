## PictureSelect


对于每个APP基本上都有一个头像上传的功能，对于如何获取头像照片，可以通过使用本地相册或者拍照获取，而是用原生的相机功能都会或多或少遇到一些问题，因此特地封装了相机和相册功能，使用简单，方便，只需要简单的几行代码就可以获取图片。



### github地址
[欢迎star、fork，点击跳转 https://github.com/crazyandcoder/TakePhoto](https://github.com/crazyandcoder/TakePhoto)


### 效果演示


![这里写图片描述](http://img.blog.csdn.net/20161026151259070)

http://upload-images.jianshu.io/upload_images/676457-2cf2314875fb6ef8.gif?imageMogr2/auto-orient/strip

### 主要亮点

 1. 可以进行拍照或者从本地相册获取图片
 2. 可以对已经选中的图片进行编辑、如裁剪、放大、缩小等操作
 3. 直接返回选中图片的地址，方便后续操作，如上传服务器等。

### v1.0.2 版本（2016.10.26）


![](http://img.blog.csdn.net/20161026140852254)

[从fir获取demo演示apk](http://fir.im/fykm)

### gradle引用

```
compile 'liji.library.dev:takephotolib:1.0.2'
```


### 代码示例（v1.0.2）

```
	  TakePhoto takePhoto = new TakePhoto(MainActivity.this);
                takePhoto.setOnPictureSelected(new TakePhoto.onPictureSelected() {
                    @Override
                    public void select(String path) {
                        textView.setText("选择的图片地址：" + path);
                        Glide.with(MainActivity.this).load("file://" + path).into(imageView);
                    }
                });
                takePhoto.show();
```

 
 


----------


**关于作者**

QQ：        275137657 
github：   https://github.com/crazyandcoder 
个人博客：http://crazyandcoder.github.io/


### 感谢

 - [galleryfinal](https://github.com/pengjianbo/GalleryFinal)
 - [ActionSheet](https://github.com/baoyongzhang/android-ActionSheet)
 - [glide](https://github.com/bumptech/glide) 
 - [universalimageloader](https://github.com/nostra13/Android-Universal-Image-Loader)
