# AnimatedGIFWriter
Standalone Android animated GIF writer.

How to use

```java
// True for dither. Will need more memory and CPU
AnimatedGIFWriter writer = new AnimatedGIFWriter(true);
OutputStream os = new FileOutputStream("animated.gif");
Bitmap bitmap; // Grab the Bitmap whatever way you can
// Use -1 for both logical screen width and height to use the first frame dimension
writer.prepareForWrite(os, -1, -1)
writer.writeFrame(os, bitmap);
// Keep adding frame here
writer.finishWrite(os);
// And you are done!!!
```

If used as normal GIF writer:

```java
// True for dither. Will need more memory and CPU
AnimatedGIFWriter writer = new AnimatedGIFWriter(true);
OutputStream os = new FileOutputStream("animated.gif");
Bitmap bitmap; // Grab the Bitmap whatever way you can
writer.writeFrame(bitmap, os);
// And you are done!!!
```
