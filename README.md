# yuv2rgbconverter
Convert Yuv Image to RGB Bitmap, helpful when using with cameraX and tensorFlow.
#### Download

```java

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
    
    
    	dependencies {
	        implementation 'com.github.trandinhquy97:yuv2rgbconverter:1.0.0'
	}
```
#### Usage

```java
    val image = imageProxy.image 
    private val yuvToRgbConverter = YuvToRgbConverter(context)
    private var bitmapBuffer = Bitmap.createBitmap(
        imageProxy.width, imageProxy.height, Bitmap.Config.ARGB_8888
    )
    yuvToRgbConverter.yuvToRgb(image, bitmapBuffer)
    Bitmap.createBitmap(
        bitmapBuffer,
        0,
        0,
        bitmapBuffer.width,
        bitmapBuffer.height,
        rotationMatrix,
        false
    )
```
